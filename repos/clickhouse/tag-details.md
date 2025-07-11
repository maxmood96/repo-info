<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.5`](#clickhouse2535)
-	[`clickhouse:25.3.5-jammy`](#clickhouse2535-jammy)
-	[`clickhouse:25.3.5.42`](#clickhouse253542)
-	[`clickhouse:25.3.5.42-jammy`](#clickhouse253542-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.10`](#clickhouse25410)
-	[`clickhouse:25.4.10-jammy`](#clickhouse25410-jammy)
-	[`clickhouse:25.4.10.45`](#clickhouse2541045)
-	[`clickhouse:25.4.10.45-jammy`](#clickhouse2541045-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.6`](#clickhouse2556)
-	[`clickhouse:25.5.6-jammy`](#clickhouse2556-jammy)
-	[`clickhouse:25.5.6.14`](#clickhouse255614)
-	[`clickhouse:25.5.6.14-jammy`](#clickhouse255614-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.3`](#clickhouse2563)
-	[`clickhouse:25.6.3-jammy`](#clickhouse2563-jammy)
-	[`clickhouse:25.6.3.116`](#clickhouse2563116)
-	[`clickhouse:25.6.3.116-jammy`](#clickhouse2563116-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.5`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.5-jammy`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.5.42`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.5.42` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.5.42` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.5.42-jammy`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.5.42-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.5.42-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.5.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.10`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.10-jammy`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.10.45`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.10.45` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.10.45` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.10.45-jammy`

```console
$ docker pull clickhouse@sha256:6f797bc0e16390ea4583da0d7e69781073dd8abc724ea84c70bf8c9377217ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.10.45-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3550157127b6fb993b86299846941278e921b8fc919916ecc5422c8dba634bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efeb75021f3af41935e5d56c91ca5f27da6dda4e8f6ad5b2743e9db1e2f6851`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a202660b52ccbf70c5153c489620ee8a03a47a3d483f3f4b603fad8e8ffff23`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f4f86c724829f3752636841ab4ce28c525da6fab610c2d83b0fa4f50654aa`  
		Last Modified: Thu, 10 Jul 2025 21:49:46 GMT  
		Size: 165.4 MB (165383808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b92f821234ea6d792886361b5f5e6fa4899b1e07e66daf02842ad25ed3a288`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75c2cd73dd5d0012827a734b4edfbeb098ddb46deed6e3b274f8fa97099d85`  
		Last Modified: Thu, 10 Jul 2025 19:57:11 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b224f43dcfd0dc64569af42206a9030fac0e2e03be0e30f74af0d4cce83233`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c996dcd843ca8ba40aa926be28f4a846ca00a46ab0ca9da68a29c88b26b20f0`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519e3d30cb082fe429733fb57fba35d4347a524a6e04197b7e2879c0f987d8c`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a65f81cfd24c5cc90022c85cad6862549b39bbe9241a61ca3af30177ed39b72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ce783d1089691e49bfbd4a5e027e548f1ddc1ff68cd171565c53bd0e06cbdb`

```dockerfile
```

-	Layers:
	-	`sha256:7f074f9f9bbe9517ecd06893482d4311211a438c504ce4c6167b7d154ab5b51a`  
		Last Modified: Thu, 10 Jul 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.10.45-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9597ec04fa1f93b29d89859af25ad475ff60cc6e301d794d0ae5cec29a213288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190215904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33236f7c9137020ae0543f6e96891585be2ce914e46aa3cb4d1557a1abd6ef64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.4.10.45
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.10.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae3e87c4c176da1e04e9da07cb2a0c8ad04284b42ac324f71a548cb41c6bfc`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 7.1 MB (7127933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a811e34447a00bb81c477e544bff9e3deb2ba6edd67d2e0667da849cdd4578b`  
		Last Modified: Thu, 10 Jul 2025 21:49:51 GMT  
		Size: 154.9 MB (154858450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344a3d1a45636c22e90b9a4d60095eb07141c3d2ee544d0b80c1f677a6a463eb`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ec39d119235078d28b0aa829ac54c7656ea52e458c3fd65d75c566c45f564`  
		Last Modified: Thu, 10 Jul 2025 19:57:56 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc248bc0002721fb3a4a0233d7d7d571ce56b924c9a566de955f6ec37f3daac`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04073a6652621df06bbd3043bb7107d95e3b674dc22b93df55a73e965ea0070c`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582478a7c95cafb746eb667a60cc7c6366377c201a5e3f989a7ca89a244b5a6`  
		Last Modified: Thu, 10 Jul 2025 19:57:55 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.10.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a5eb496dd8fbef442a3d0207111956d06da8441bcdef7849666bebe4ad67007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384bf970adb01cceeb147e85d59fddcc3e6b16468f4aca21908fe9d4e77d306`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a1b60f4c4a1d7c8013a022ca763bafee976c73e4e3e477679403f531386b7`  
		Last Modified: Thu, 10 Jul 2025 21:49:26 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.6`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.6-jammy`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.6.14`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.6.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.6.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.6.14-jammy`

```console
$ docker pull clickhouse@sha256:11bd44a8c840b56dda7735e2e72b4a1095f68b621d713219864c3ca0543d6fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.6.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:65a9578e65fe02e9518cd69d6b8937b55a208b14080860be7d26727af3cd5e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205087083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568db497aa1f45bc5246e60c821b508b1f8f257ff6375ad7c95c4201c4aeae2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581fa3e14e5d66c6bc9f29d2aea5a871184909660443fdbb9bbc974a1c767bb`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 7.2 MB (7151657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da02049a0bdbc49a186ca9d5651fc442aeaaa0b5592a07a4f40b444856800c`  
		Last Modified: Mon, 07 Jul 2025 21:50:10 GMT  
		Size: 167.5 MB (167529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd7fc8c5334767f5c964b4224a52352feab7f76c0fe8102747fcd747b032e8`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bd5c22724fc5b6e6887caeb11a64356cc744b97d18cf49e9796aca05c2258`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c68562391c1dfc8549b70b7eac6c356b30c2c0aafb7d334dc412409ea5a4`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0125ddbe3243b1b4f0d19d030e00f1be215687bf2e1a0839032ac36ca4bb22`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ddfb2a05ac0aef96815368a8a2aef952a5428970cb533f02e1bc61f051393`  
		Last Modified: Mon, 07 Jul 2025 20:22:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b0c42cae7f2551734a96a4c6ca054c60190be5ef4c8a4341f9fa74a15367c1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d41f28b9accfd12f1f766b12d643fca4d3602ac913fc0a938791f8f4cee5423`

```dockerfile
```

-	Layers:
	-	`sha256:f602b29dbbb9ac5c86bd43d5fecb7f225e95777246db8e41d2f3bb2f499e61c3`  
		Last Modified: Mon, 07 Jul 2025 21:49:45 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.6.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6a48f81b7d4a8a363fbd66bae6ed3179e1171bcdcb4f4e920990750d148b9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191655731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c7e6263f719a01c6dc245e764b270e7b9ac147e53c556308a42131d6fd4de2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.5.6.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.6.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66b9cca759ca58a40a10e0b6fcaed1606884a4de06e0dc71c60ff621ca2967`  
		Last Modified: Mon, 07 Jul 2025 21:50:13 GMT  
		Size: 156.3 MB (156298301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46847e6474e2470c24717c3201cdcb0986b13838e005ef4b5f41328660fb370d`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66230cb2917108d327b9824e8b4d8c4253a06c9f42ef4a865460f47e5d267206`  
		Last Modified: Mon, 07 Jul 2025 20:24:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8492761af2be5bb3809db5a657516576c660c90098bfa118fee71a2087f5f7`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae27b9f75e540eedd01566988c451b278b8285f9de900d0e38860cda97ff98`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0efbf26a98804ec20bbaa6db500ad6eb0860ced06f36f21fc422e171b950c`  
		Last Modified: Mon, 07 Jul 2025 20:23:56 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.6.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a2aaedc8df148eb91e7782d702b2cc6aab1205fe76f1b44a304fe328d7ae51ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ec52407f141dbfecc22a573c628c20518c6a6bb7fe87478c5dab311553312e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee77534a988bab0dc53957b94d4458f409f1b48b451e040a036439bcc96c6ec`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.3`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.3-jammy`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.3.116`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.3.116` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3.116` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.3.116` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3.116` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.3.116-jammy`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.3.116-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3.116-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.3.116-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.3.116-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:0fc6bcb9a5e2c60d3d723fb84dca387ff079ef4337d97f281cef76f523086ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e0abb144ef6eb3e9625bbac9e7d65dc473bc5ced7fb3b365af802646945a1ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205569292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34938ef3f36fdffa94e2b714a7efa1702437139ef47a580e8e1b545682dff4ce`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a3864295c408b2f5a45f2a7949712fcc1e3ea1d11293c37905649a2868ddf`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92ccc9fe4a46f96f5ede04c450ccfe9de9339a3c66745c5ad8b192f7d85398f`  
		Last Modified: Mon, 07 Jul 2025 21:49:48 GMT  
		Size: 168.0 MB (168011738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88457dcd94ff79326c5a3a08e38f3fa1de91997ac5cfbfc8a1e79d5416ee52`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc6b5518565f8c4e3e35ecd1f5b9434de60acd0af42ef0c0d76abd74f9f589`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd09224522bb457d02b57b004751853c09e3ebbf38550e609abbecc4f1f6b20`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07adf6fc741806e30579441c3339c2168c6ad8c10cd2630d56836214bb0f4dcf`  
		Last Modified: Mon, 07 Jul 2025 20:23:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730640cbc31e718b1c25c14c094d6141463f7c3b7fd0a193744aff90070d5505`  
		Last Modified: Mon, 07 Jul 2025 20:23:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:260a7f5da180ee28204ce3ca07278e7eebf88661b8dd15c5fd444a7e7df47bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2568cc1e0f70ed3275e42c29666897308bbbcb3ec3f66269a8bdbe54d56c3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:3c83df8ba1ae311ae8342a60c0a3c31979b9731b9f6b21f92100a39035f54b50`  
		Last Modified: Mon, 07 Jul 2025 21:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:94b874954ff1c222c9186fadef3b8a8dba99d7876067c8ce9b929468c1533e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193052270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b674bca065cfb4bac6672f19467de4866b836ed54f8188d3aa177c419d17fd3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 04 Jul 2025 11:31:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 04 Jul 2025 11:31:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 04 Jul 2025 11:31:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 04 Jul 2025 11:31:38 GMT
ARG VERSION=25.3.5.42
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.5.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 04 Jul 2025 11:31:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 04 Jul 2025 11:31:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 04 Jul 2025 11:31:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ebcc2e32eb5c83b4b49e0d386849a84001af9e4ca2176bc4fe389ef1fdc00`  
		Last Modified: Mon, 07 Jul 2025 20:22:53 GMT  
		Size: 7.1 MB (7127908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e95b46eff64a3b0ed0ff2bf1f8ec8449cf584471cb3f8c48552deafecedc`  
		Last Modified: Mon, 07 Jul 2025 21:49:40 GMT  
		Size: 157.7 MB (157694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2702af1bf587338b516c80e54acbd75a421b9a7ba9f3584e6328951f55ad9ab6`  
		Last Modified: Mon, 07 Jul 2025 20:25:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4957464480a095e0f750368164e04a91761df5216bff8120e4e48aceae448d9b`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b7875e1d00d1ccfc12b0b83a96ce0b5914b2f67ba44e302cb796db391ded`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58e6aeb0197f24570b9f5857157fe927f90f1517d63d727fe95b3643d93734`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb5fd598474845db517a93663263d1208124b78da54efa803fc79a4214bacf`  
		Last Modified: Mon, 07 Jul 2025 20:25:36 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e505491604e343483b80b45b7c5d55217c07096f30d4a4122775957e2145e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d4717a51273367da76af4936ea2db75be0b93f1f1cdd76b649b44c2c7839a`

```dockerfile
```

-	Layers:
	-	`sha256:68ecf339629c23e4d46b5f4a70e16f4fdad190ac759333c9538307439792bbdc`  
		Last Modified: Mon, 07 Jul 2025 21:49:24 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
