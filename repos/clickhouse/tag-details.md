<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.4`](#clickhouse2534)
-	[`clickhouse:25.3.4-jammy`](#clickhouse2534-jammy)
-	[`clickhouse:25.3.4.190`](#clickhouse2534190)
-	[`clickhouse:25.3.4.190-jammy`](#clickhouse2534190-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.7`](#clickhouse2547)
-	[`clickhouse:25.4.7-jammy`](#clickhouse2547-jammy)
-	[`clickhouse:25.4.7.66`](#clickhouse254766)
-	[`clickhouse:25.4.7.66-jammy`](#clickhouse254766-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.4`](#clickhouse2554)
-	[`clickhouse:25.5.4-jammy`](#clickhouse2554-jammy)
-	[`clickhouse:25.5.4.38`](#clickhouse255438)
-	[`clickhouse:25.5.4.38-jammy`](#clickhouse255438-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.1`](#clickhouse2561)
-	[`clickhouse:25.6.1-jammy`](#clickhouse2561-jammy)
-	[`clickhouse:25.6.1.3206`](#clickhouse25613206)
-	[`clickhouse:25.6.1.3206-jammy`](#clickhouse25613206-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.4`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.4-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.4.190`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.4.190-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7.66`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7.66` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7.66` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7.66-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7.66-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7.66-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:66cba64a0df1c18ad49bdb75bb8c7458b39583c94529fdea3dfa2751a88404db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:63b46c16de87d8bc02d01d6965c6aac3d0a80922497a1546ac2071aab036382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204926746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37169576133d2bd56a92fc21c2e7a2505170099253126f6e3cb1f64d8130993f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b056136d88b3297b466c9b882af3235e51d03c45952cd9a42950987038a0d`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 7.2 MB (7151665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbb24ffb20b9c98251da6cd27ccd7b258b90f782168382f9558855260ddbbb4`  
		Last Modified: Fri, 20 Jun 2025 21:50:08 GMT  
		Size: 167.4 MB (167371832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf255bd33cb46cc2436be97c73c289e8aba41065a7aa1cab943b5c703286463`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c29fc85f9d64a067d3ac89051f5575f5abfa5ee4d4fb27320e6bf71ae25904`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7071bbbec19adf5a3c6553dc197e88a3c2abcd1013c6bc8459959891fdb52e7`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dce08734f30bc3d4b1cb075b139e0c9f8ba72ed2e83e1f387f4aec0eb04ff`  
		Last Modified: Fri, 20 Jun 2025 19:09:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaffe32b946e557b7cdf66580b97ce7cf5a1e530932938dc45f7a1daa171c02`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6bfeb4d250197c24c1dd7cff9efe58ee47f908b204265b5ab75494082bbd00a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcb3321ca7eea034aaeca639db1aecfa97e12950b3d9184989e29c43545473`

```dockerfile
```

-	Layers:
	-	`sha256:a103f01a4226c04a60b22e8dd5a8ae67cf24d852af8387226100b1a5e2970f09`  
		Last Modified: Fri, 20 Jun 2025 21:49:38 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dceb3d2af8f38db81e5b04b355e32c1376a45b9fe35037709a72b5202f91b210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ba4709f2323470e9716871250c74011970599f5d77bfeab3d4cfc04f2595d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb906d94c89901e391a787129dce02a577bb828206d252b193953a5ab28d9ad`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a151e5d112564c0b052629a04a4c590f13298862bb891e7c45825220d94b5c`  
		Last Modified: Fri, 20 Jun 2025 21:50:02 GMT  
		Size: 156.1 MB (156145196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb1a3d62599404306baba385babc1c49c09851004e442ed38412c5a55aad6bd`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756b9d24d15787be3faa13ba8bd36b9e7a547099d0cd9de411434f5d8b071e7`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2884d60e2563049c647dbc163fbc8584ece7e7fd3d6075827b774df9da5bd6`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661d1cf06749982a0d79df157a1b0d9e3536085d1e59560ae59cbc46062ac7e`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa7aaf467208cf1091f9b3289865e5259ce56d3c330beae28ee2d9ad97947a`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23a52ac527152b19f35c732786a9623124e4c239610b0d64cc856955a53fdfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e6b10dc30dd0c90aeda4913ef77cc4de4499dfa886f51013273602659064e`

```dockerfile
```

-	Layers:
	-	`sha256:89361c1ca1ae0cf5f3ec11107ce689f64fdf0745e0620ea2bacab809518b71be`  
		Last Modified: Fri, 20 Jun 2025 21:49:42 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:66cba64a0df1c18ad49bdb75bb8c7458b39583c94529fdea3dfa2751a88404db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:63b46c16de87d8bc02d01d6965c6aac3d0a80922497a1546ac2071aab036382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204926746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37169576133d2bd56a92fc21c2e7a2505170099253126f6e3cb1f64d8130993f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b056136d88b3297b466c9b882af3235e51d03c45952cd9a42950987038a0d`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 7.2 MB (7151665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbb24ffb20b9c98251da6cd27ccd7b258b90f782168382f9558855260ddbbb4`  
		Last Modified: Fri, 20 Jun 2025 21:50:08 GMT  
		Size: 167.4 MB (167371832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf255bd33cb46cc2436be97c73c289e8aba41065a7aa1cab943b5c703286463`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c29fc85f9d64a067d3ac89051f5575f5abfa5ee4d4fb27320e6bf71ae25904`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7071bbbec19adf5a3c6553dc197e88a3c2abcd1013c6bc8459959891fdb52e7`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dce08734f30bc3d4b1cb075b139e0c9f8ba72ed2e83e1f387f4aec0eb04ff`  
		Last Modified: Fri, 20 Jun 2025 19:09:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaffe32b946e557b7cdf66580b97ce7cf5a1e530932938dc45f7a1daa171c02`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6bfeb4d250197c24c1dd7cff9efe58ee47f908b204265b5ab75494082bbd00a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcb3321ca7eea034aaeca639db1aecfa97e12950b3d9184989e29c43545473`

```dockerfile
```

-	Layers:
	-	`sha256:a103f01a4226c04a60b22e8dd5a8ae67cf24d852af8387226100b1a5e2970f09`  
		Last Modified: Fri, 20 Jun 2025 21:49:38 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dceb3d2af8f38db81e5b04b355e32c1376a45b9fe35037709a72b5202f91b210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ba4709f2323470e9716871250c74011970599f5d77bfeab3d4cfc04f2595d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb906d94c89901e391a787129dce02a577bb828206d252b193953a5ab28d9ad`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a151e5d112564c0b052629a04a4c590f13298862bb891e7c45825220d94b5c`  
		Last Modified: Fri, 20 Jun 2025 21:50:02 GMT  
		Size: 156.1 MB (156145196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb1a3d62599404306baba385babc1c49c09851004e442ed38412c5a55aad6bd`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756b9d24d15787be3faa13ba8bd36b9e7a547099d0cd9de411434f5d8b071e7`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2884d60e2563049c647dbc163fbc8584ece7e7fd3d6075827b774df9da5bd6`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661d1cf06749982a0d79df157a1b0d9e3536085d1e59560ae59cbc46062ac7e`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa7aaf467208cf1091f9b3289865e5259ce56d3c330beae28ee2d9ad97947a`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23a52ac527152b19f35c732786a9623124e4c239610b0d64cc856955a53fdfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e6b10dc30dd0c90aeda4913ef77cc4de4499dfa886f51013273602659064e`

```dockerfile
```

-	Layers:
	-	`sha256:89361c1ca1ae0cf5f3ec11107ce689f64fdf0745e0620ea2bacab809518b71be`  
		Last Modified: Fri, 20 Jun 2025 21:49:42 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.4`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.5.4-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.5.4.38`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.5.4.38-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6.1`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6.1-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6.1.3206`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.6.1.3206-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:66cba64a0df1c18ad49bdb75bb8c7458b39583c94529fdea3dfa2751a88404db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:63b46c16de87d8bc02d01d6965c6aac3d0a80922497a1546ac2071aab036382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204926746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37169576133d2bd56a92fc21c2e7a2505170099253126f6e3cb1f64d8130993f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b056136d88b3297b466c9b882af3235e51d03c45952cd9a42950987038a0d`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 7.2 MB (7151665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbb24ffb20b9c98251da6cd27ccd7b258b90f782168382f9558855260ddbbb4`  
		Last Modified: Fri, 20 Jun 2025 21:50:08 GMT  
		Size: 167.4 MB (167371832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf255bd33cb46cc2436be97c73c289e8aba41065a7aa1cab943b5c703286463`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c29fc85f9d64a067d3ac89051f5575f5abfa5ee4d4fb27320e6bf71ae25904`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7071bbbec19adf5a3c6553dc197e88a3c2abcd1013c6bc8459959891fdb52e7`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dce08734f30bc3d4b1cb075b139e0c9f8ba72ed2e83e1f387f4aec0eb04ff`  
		Last Modified: Fri, 20 Jun 2025 19:09:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaffe32b946e557b7cdf66580b97ce7cf5a1e530932938dc45f7a1daa171c02`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6bfeb4d250197c24c1dd7cff9efe58ee47f908b204265b5ab75494082bbd00a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcb3321ca7eea034aaeca639db1aecfa97e12950b3d9184989e29c43545473`

```dockerfile
```

-	Layers:
	-	`sha256:a103f01a4226c04a60b22e8dd5a8ae67cf24d852af8387226100b1a5e2970f09`  
		Last Modified: Fri, 20 Jun 2025 21:49:38 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dceb3d2af8f38db81e5b04b355e32c1376a45b9fe35037709a72b5202f91b210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ba4709f2323470e9716871250c74011970599f5d77bfeab3d4cfc04f2595d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb906d94c89901e391a787129dce02a577bb828206d252b193953a5ab28d9ad`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a151e5d112564c0b052629a04a4c590f13298862bb891e7c45825220d94b5c`  
		Last Modified: Fri, 20 Jun 2025 21:50:02 GMT  
		Size: 156.1 MB (156145196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb1a3d62599404306baba385babc1c49c09851004e442ed38412c5a55aad6bd`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756b9d24d15787be3faa13ba8bd36b9e7a547099d0cd9de411434f5d8b071e7`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2884d60e2563049c647dbc163fbc8584ece7e7fd3d6075827b774df9da5bd6`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661d1cf06749982a0d79df157a1b0d9e3536085d1e59560ae59cbc46062ac7e`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa7aaf467208cf1091f9b3289865e5259ce56d3c330beae28ee2d9ad97947a`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23a52ac527152b19f35c732786a9623124e4c239610b0d64cc856955a53fdfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e6b10dc30dd0c90aeda4913ef77cc4de4499dfa886f51013273602659064e`

```dockerfile
```

-	Layers:
	-	`sha256:89361c1ca1ae0cf5f3ec11107ce689f64fdf0745e0620ea2bacab809518b71be`  
		Last Modified: Fri, 20 Jun 2025 21:49:42 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:66cba64a0df1c18ad49bdb75bb8c7458b39583c94529fdea3dfa2751a88404db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:63b46c16de87d8bc02d01d6965c6aac3d0a80922497a1546ac2071aab036382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204926746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37169576133d2bd56a92fc21c2e7a2505170099253126f6e3cb1f64d8130993f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2b056136d88b3297b466c9b882af3235e51d03c45952cd9a42950987038a0d`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 7.2 MB (7151665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbb24ffb20b9c98251da6cd27ccd7b258b90f782168382f9558855260ddbbb4`  
		Last Modified: Fri, 20 Jun 2025 21:50:08 GMT  
		Size: 167.4 MB (167371832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf255bd33cb46cc2436be97c73c289e8aba41065a7aa1cab943b5c703286463`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c29fc85f9d64a067d3ac89051f5575f5abfa5ee4d4fb27320e6bf71ae25904`  
		Last Modified: Fri, 20 Jun 2025 19:09:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7071bbbec19adf5a3c6553dc197e88a3c2abcd1013c6bc8459959891fdb52e7`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dce08734f30bc3d4b1cb075b139e0c9f8ba72ed2e83e1f387f4aec0eb04ff`  
		Last Modified: Fri, 20 Jun 2025 19:09:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaffe32b946e557b7cdf66580b97ce7cf5a1e530932938dc45f7a1daa171c02`  
		Last Modified: Fri, 20 Jun 2025 19:09:36 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6bfeb4d250197c24c1dd7cff9efe58ee47f908b204265b5ab75494082bbd00a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dcb3321ca7eea034aaeca639db1aecfa97e12950b3d9184989e29c43545473`

```dockerfile
```

-	Layers:
	-	`sha256:a103f01a4226c04a60b22e8dd5a8ae67cf24d852af8387226100b1a5e2970f09`  
		Last Modified: Fri, 20 Jun 2025 21:49:38 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dceb3d2af8f38db81e5b04b355e32c1376a45b9fe35037709a72b5202f91b210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ba4709f2323470e9716871250c74011970599f5d77bfeab3d4cfc04f2595d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.5.3.75
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.3.75 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb906d94c89901e391a787129dce02a577bb828206d252b193953a5ab28d9ad`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a151e5d112564c0b052629a04a4c590f13298862bb891e7c45825220d94b5c`  
		Last Modified: Fri, 20 Jun 2025 21:50:02 GMT  
		Size: 156.1 MB (156145196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb1a3d62599404306baba385babc1c49c09851004e442ed38412c5a55aad6bd`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756b9d24d15787be3faa13ba8bd36b9e7a547099d0cd9de411434f5d8b071e7`  
		Last Modified: Fri, 20 Jun 2025 20:31:23 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2884d60e2563049c647dbc163fbc8584ece7e7fd3d6075827b774df9da5bd6`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661d1cf06749982a0d79df157a1b0d9e3536085d1e59560ae59cbc46062ac7e`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa7aaf467208cf1091f9b3289865e5259ce56d3c330beae28ee2d9ad97947a`  
		Last Modified: Fri, 20 Jun 2025 20:31:22 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23a52ac527152b19f35c732786a9623124e4c239610b0d64cc856955a53fdfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e6b10dc30dd0c90aeda4913ef77cc4de4499dfa886f51013273602659064e`

```dockerfile
```

-	Layers:
	-	`sha256:89361c1ca1ae0cf5f3ec11107ce689f64fdf0745e0620ea2bacab809518b71be`  
		Last Modified: Fri, 20 Jun 2025 21:49:42 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json
