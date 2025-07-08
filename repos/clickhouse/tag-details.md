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
-	[`clickhouse:25.4.9`](#clickhouse2549)
-	[`clickhouse:25.4.9-jammy`](#clickhouse2549-jammy)
-	[`clickhouse:25.4.9.14`](#clickhouse254914)
-	[`clickhouse:25.4.9.14-jammy`](#clickhouse254914-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.6`](#clickhouse2556)
-	[`clickhouse:25.5.6-jammy`](#clickhouse2556-jammy)
-	[`clickhouse:25.5.6.14`](#clickhouse255614)
-	[`clickhouse:25.5.6.14-jammy`](#clickhouse255614-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.2`](#clickhouse2562)
-	[`clickhouse:25.6.2-jammy`](#clickhouse2562-jammy)
-	[`clickhouse:25.6.2.5`](#clickhouse25625)
-	[`clickhouse:25.6.2.5-jammy`](#clickhouse25625-jammy)
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
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.9`

```console
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.9-jammy`

```console
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.9.14`

```console
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.9.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.9.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.9.14-jammy`

```console
$ docker pull clickhouse@sha256:8a5da7448b36b43f7d2206f557f06803bdf011213f1f0cd29baf1edf0cd403f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.9.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8026c83248bf91be6a1d72c92b02571509b1f85bedffa025296e2ff38e73b8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202930344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecf326b920e275844b64fcfc49d2e61396d15bde9eef0594d057014562c75d5`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:e4250c10f09ad2b30cd80b348b995fe7ad6ef264ff6458cf8f5ef55e6a752e38`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e706612ba74a42530c44e14947d7c781f9f0753014d89f1db94267d92eae04`  
		Last Modified: Mon, 07 Jul 2025 21:49:54 GMT  
		Size: 165.4 MB (165372811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d04c4f4584dbf9d35d15d3e61bc916ae88c46b238f9fb9d9baefebdd865e9c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b30dd3c432159d87db9ca545c9bff4ffc60686d6730c7abae587e4042324c`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47db4be0e881a27b8ab2b95da9faf4a88a989a6d50cbdee122e56b506db80eb4`  
		Last Modified: Mon, 07 Jul 2025 20:23:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc440591809adcd2a887c10ca9bf5adc6acb28e6b2fe912947c4d6ef69677239`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fb644d1a048b56dfc0b8c3b06da191df4d733e62479e7b9dc1364aea7beec`  
		Last Modified: Mon, 07 Jul 2025 20:23:24 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd33a65edb161b33e8c6e7aad68f5bde8da0fa3c8a35d8bff03440a116268003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ab66431df0f6feecba0128cfe960406e6c12be2f1c1fe882994439ba4047`

```dockerfile
```

-	Layers:
	-	`sha256:e3d1cda29eb0158d6c34774d5145d254403ff2fbfdf05665ff668c04bfa3eeb2`  
		Last Modified: Mon, 07 Jul 2025 21:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.9.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63067e35f94263e56b0ee1b5e66cde459eb31929f5ceaae2e3a226d6220d2810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190204017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1720f7f834d12a6a6cb7d2ce199d191bb634b2248419c84aba599cf9998958f7`
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
ARG VERSION=25.4.9.14
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:b125aaed011be6e56dcda14d07338cce5734f1aa234b83bfe9a171e5092b9456`  
		Last Modified: Mon, 07 Jul 2025 21:49:53 GMT  
		Size: 154.8 MB (154846588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16aef339de27471904f08895ea046f55377d53a8be1b78f8ef713370a882fd4`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828e85c885f370d7ebf8ea5694654d504396aa5100d95654695ca81daae7353`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298abe77af6f14c9e32abe240720e41ddcb2a10e3cef1f732ace9afc5bc54c2`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74219c80a8097fe7b0635bb3bee9ff38503a06aaa7ceff3e93e1995a1be26ea`  
		Last Modified: Mon, 07 Jul 2025 20:24:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8b3c4469bf5356fafb0a313571185512ca37a52034b7e9b02703e89e2a14b`  
		Last Modified: Mon, 07 Jul 2025 20:24:31 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.9.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53ba28d9d36b1a0ffa755058d50950da4cb3fcec1e9cbabdacc2fe91d9f9da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1857d942b0e60c7dfced72d79daa9db038dbb428122e54a7fcfeb4f6e81f56`

```dockerfile
```

-	Layers:
	-	`sha256:a1dd5a44d13be11ef699a029450a4593deaedf54e9dea6dc31aab078b4a21140`  
		Last Modified: Mon, 07 Jul 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
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
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.2`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.2-jammy`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.2.5`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.2.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.2.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.2.5-jammy`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.2.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.2.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:9e3411eacb7a1093083952f67413429e839aad3e39475a52fc38321cd571e79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:68490dc3c49a014b5598394203f161886c11dcef6e8aa25cb79fc291ddc94a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab46a7171d32b2e34fd02f2236b6371153b49be7c1017152da80a25f613b7c95`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:7285bf5904218bb76b6bbe0670b051095ad113d7c5e37c064573c4f4c17bc8de`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 7.2 MB (7151601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5060df7522e6b9b11fb4b061508ee3257071a58f19e11ccff639fd18dd63ba90`  
		Last Modified: Mon, 07 Jul 2025 21:50:21 GMT  
		Size: 174.5 MB (174529400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f0f861f6c228d8f18ad63560b9592df94bb7fc712e8c2dfe46bac9175ebf4`  
		Last Modified: Mon, 07 Jul 2025 20:22:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11a31a6effe08afbd063d6b7462ae0f7b97edbf687a6856b4c2d224724fc38`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e060627c415a2e5d933cf50a12dcdd8787a94c89af6794177a4d79ef09b219`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3d859a4ff74c49f4ce10ae7b98b896fb1f5882d1dd8b52433da0b07e7591d`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3022911f50dbe73469407647db7ffc192e05eb3ec79e0ce2f52edf3ebfab7f`  
		Last Modified: Mon, 07 Jul 2025 20:22:45 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9e2912a58a5b8dd7ab8a272707bebd0e7c2f38a39aaa44fd8c4a55a4c35caf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c39747524923ae4b81c0885e2e1dd673fe21908f62acc715c0fa9dcab09e149`

```dockerfile
```

-	Layers:
	-	`sha256:42f3581d4315626edf36504083a987922020ceba44ba4cb0479e46e2b4118c89`  
		Last Modified: Mon, 07 Jul 2025 21:49:58 GMT  
		Size: 25.9 KB (25862 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26abfb7a6653d2647bf43b4cf009fd1c2f24cf92268407fb04195a32c1c7390b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198245457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae06bd6a3571ba759c5f5d7f39f077f7ff89daba9b574d7cfd6f67fa0d15f54`
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
ARG VERSION=25.6.2.5
# Fri, 04 Jul 2025 11:31:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 04 Jul 2025 11:31:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jul 2025 11:31:38 GMT
ENV TZ=UTC
# Fri, 04 Jul 2025 11:31:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.2.5 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:45c9ead8fe4bb4b154b386893f4b9d149ab50613b3b396c6e425ad9687790d72`  
		Last Modified: Mon, 07 Jul 2025 21:50:22 GMT  
		Size: 162.9 MB (162888254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2620f8248f570faddc5083a9c450a72437d6ded6ef901f83300e5fcbb164a18`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b3f1c9063becdbe9e674a25023c24e0ddaecb10f347450ba88f158ba85965`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5c0c93de4444bf27dd24bba2489a8cfefc7dbfbf5f50cec0961218fbd677c`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450daa6e3bc27064ea9e2836c43259165fb328abc7954c13f9b346c11fad4fef`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896124542215e131e75c0c55daab3a117bcd5aa7f8586ca92569eac7c28b1778`  
		Last Modified: Mon, 07 Jul 2025 20:22:52 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc84eefdf14dec6c8978402eee6b105ce723b7c055b408e255c1b07a8dbf8415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d87174db11374a358e2b7d1ab6135ec508779923fd70cac5c2347b2d16178e0`

```dockerfile
```

-	Layers:
	-	`sha256:11fc25949ea2b3030cd93795db209250e10c5813986e1acb63a34dc7a65f6dd9`  
		Last Modified: Mon, 07 Jul 2025 21:50:02 GMT  
		Size: 26.1 KB (26074 bytes)  
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
