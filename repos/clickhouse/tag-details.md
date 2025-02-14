<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.10`](#clickhouse2410)
-	[`clickhouse:24.10-focal`](#clickhouse2410-focal)
-	[`clickhouse:24.10.4`](#clickhouse24104)
-	[`clickhouse:24.10.4-focal`](#clickhouse24104-focal)
-	[`clickhouse:24.10.4.191`](#clickhouse24104191)
-	[`clickhouse:24.10.4.191-focal`](#clickhouse24104191-focal)
-	[`clickhouse:24.11`](#clickhouse2411)
-	[`clickhouse:24.11-jammy`](#clickhouse2411-jammy)
-	[`clickhouse:24.11.3`](#clickhouse24113)
-	[`clickhouse:24.11.3-jammy`](#clickhouse24113-jammy)
-	[`clickhouse:24.11.3.66`](#clickhouse2411366)
-	[`clickhouse:24.11.3.66-jammy`](#clickhouse2411366-jammy)
-	[`clickhouse:24.12`](#clickhouse2412)
-	[`clickhouse:24.12-jammy`](#clickhouse2412-jammy)
-	[`clickhouse:24.12.3`](#clickhouse24123)
-	[`clickhouse:24.12.3-jammy`](#clickhouse24123-jammy)
-	[`clickhouse:24.12.3.47`](#clickhouse2412347)
-	[`clickhouse:24.12.3.47-jammy`](#clickhouse2412347-jammy)
-	[`clickhouse:24.3`](#clickhouse243)
-	[`clickhouse:24.3-focal`](#clickhouse243-focal)
-	[`clickhouse:24.3.15`](#clickhouse24315)
-	[`clickhouse:24.3.15-focal`](#clickhouse24315-focal)
-	[`clickhouse:24.3.15.72`](#clickhouse2431572)
-	[`clickhouse:24.3.15.72-focal`](#clickhouse2431572-focal)
-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.12`](#clickhouse24812)
-	[`clickhouse:24.8.12-focal`](#clickhouse24812-focal)
-	[`clickhouse:24.8.12.28`](#clickhouse2481228)
-	[`clickhouse:24.8.12.28-focal`](#clickhouse2481228-focal)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-focal`](#clickhouselts-focal)

## `clickhouse:24.10`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10-focal`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.4`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.4-focal`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.4-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.4-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.4.191`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.4.191` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4.191` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.4.191` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4.191` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.4.191-focal`

```console
$ docker pull clickhouse@sha256:2a1d284cb69ed2ed79c787f555213668c6110bbdd1cfeff843757cecd40dc846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.4.191-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:d06b83dd697934ad6b38c96aa9573f4321af30acc9ca053603d247b41f31d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180601506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6829075fbe91d338020a82da6e39d528257f9f4b06807490dc05bf4861172`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3be90c5eca462576a467b1e22eb2e2f3a94ef19243c68bf6a4f9985f848546d`  
		Last Modified: Wed, 05 Feb 2025 17:17:53 GMT  
		Size: 8.8 MB (8802632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f098d7a0affbd6b93009c4e5bf474e90c4d24ad83fe61551969845119c7de26`  
		Last Modified: Mon, 10 Feb 2025 05:29:39 GMT  
		Size: 143.4 MB (143420538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdfd6e06f4a0d549e2fc5e07092803800114e5ac3d2c708ef9453bc25f3b53`  
		Last Modified: Fri, 07 Feb 2025 13:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89098d18e48492840e6c9cdd16a48a66f913e1e6d2f894cf377f97299e3d9f5b`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93b434c001fb9045a3bb1110607e6a5bf4915e34b9bc66af8fa1e0ba1e869c`  
		Last Modified: Wed, 05 Feb 2025 17:17:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30527fc2af174c1a09166b3928787f2b81abc15f9a740b68d24235327b5bf2`  
		Last Modified: Wed, 05 Feb 2025 17:18:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4.191-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9377d67318fb6060fa200ed969c3a4cc8484e0b5e98bfef136ce0237ace7d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18497d82b09d9ac4ce4bafaa7b63d9fe4733e2141e9285871bab725edb46e30`

```dockerfile
```

-	Layers:
	-	`sha256:af32c78e1eb9389a2c4b9d280a2fb91bda00a13d9fb6cae09093d6d8eb5f0ca5`  
		Last Modified: Wed, 15 Jan 2025 22:29:27 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.4.191-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cdb491b35636a76452a54598ebcce3e8004293c180e3fab55195617298a9a501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174235389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95520b336787b8f7a5672ac84b2b57ab1f978657db466905ef29fe24a79442b3`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.10.4.191
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.4.191 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d35a179e58ce5005218ecf8998e126f0479aad735ee8843180b4fa7b2d81ad`  
		Last Modified: Tue, 04 Feb 2025 21:38:52 GMT  
		Size: 138.7 MB (138731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a16c95b0199d75b84141c05c96598a8385ff9238d96d164b942b6945b84edc`  
		Last Modified: Mon, 10 Feb 2025 20:12:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2f23a18237be4b127685cf5ae19997ab1f347820857da25b702160d73512f`  
		Last Modified: Mon, 03 Feb 2025 23:58:28 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f178ec931c639c6021c2b77f3f5cc83e847f1e14b54694c91f26b118824632`  
		Last Modified: Wed, 05 Feb 2025 16:11:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761104cc69944f3ae975991e4ba40be5675fba5a0d4cac8c163c90dcbf5d9975`  
		Last Modified: Mon, 03 Feb 2025 22:00:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9085d650ef0eeea7b31a4861b29c6dc6029fd1c99a4f6c0f8fb0f0a6f2a5c24`  
		Last Modified: Thu, 06 Feb 2025 23:01:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.4.191-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ac7ecebca23beb73abd19f9fac3c342cb25a547e542c9184ed7a83a22a5d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc56850173ce4b05f773edbbf23107fe788db01fc798bcdede5d5293cba359`

```dockerfile
```

-	Layers:
	-	`sha256:9698cf7d9e99e1e893836d5733ef11ff5f7718f812aef1911a08fa306cd262f3`  
		Last Modified: Wed, 15 Jan 2025 22:33:51 GMT  
		Size: 25.5 KB (25485 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11-jammy`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.3`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.3-jammy`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.3.66`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.3.66` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.3.66` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.3.66-jammy`

```console
$ docker pull clickhouse@sha256:78d164d482e6f084535cb093246e2fa498685fb8bac8dd1b2fe24e4e7a466eb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.3.66-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b60105522989e0bd43f8a4abcbd61934d11eef644168565575682f4849c2b914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182665554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396beaf36eabef0a5352f3458398f63d02a2ba7bcb5d8e1fa2e282c4a8bcb0ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db63368b06316c62a7a277a48ad18a6aefd4de6c915ce107e736c8741d3f046`  
		Last Modified: Wed, 05 Feb 2025 10:00:18 GMT  
		Size: 7.1 MB (7147449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ab68423379fb2f6fd8a8a2328b7e654cf52271b206ec74540ea032a8dfcc40`  
		Last Modified: Wed, 05 Feb 2025 08:45:11 GMT  
		Size: 145.1 MB (145112608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef0464529947968c89c0d3c63d1db2387918f40c69953be7d52c513a2253`  
		Last Modified: Thu, 06 Feb 2025 02:02:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58fafea3a1569ecd0acdeef6a978b710a03ae421b31474bfe3e9bfddbe4889`  
		Last Modified: Thu, 06 Feb 2025 02:02:22 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71235424e2f3ea53352a7bdffab522db3ab925808e150ebe3984f5b3d273db5`  
		Last Modified: Thu, 06 Feb 2025 02:02:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd650c1ef1bd821128a41cec891f5f10dc2ada8aa2beab482d3971742a3d14a6`  
		Last Modified: Thu, 06 Feb 2025 02:02:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a615f2717a970111cbee10ec917bb53cdbc255ed618cb797f6f629445ef66e2`  
		Last Modified: Tue, 04 Feb 2025 05:40:55 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2890a83555578054abce5feaad46ddfedaf23385e4bf9dbd7cb62914b87788b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5151ab542dcc4e17c3e80d2950a86251e2542f1ba4ee9f49839943ed6ac2a088`

```dockerfile
```

-	Layers:
	-	`sha256:123a80acc51063a54de3f424aa937db5c4f1b941f384b7546a6eff9a828120ef`  
		Last Modified: Thu, 06 Feb 2025 02:02:40 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.3.66-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3c3b396796865ab91df8977e1eea7a2e64ecb74f3a87790c50c477b5984c0e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172827413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dfea0f3662fd2f6f08cd7d0136bab10137ec75210c3f65764da21359437eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.11.3.66
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.3.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d98a1d3e8887919b07c4b172ce9c1ae4942cff0ea8c09383e8abe0e87f95894`  
		Last Modified: Thu, 06 Feb 2025 02:03:20 GMT  
		Size: 137.5 MB (137478532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb752145057eea342a5dfc0e3d198b67cdbc04cb1619848f7de9671e2962c0e5`  
		Last Modified: Thu, 06 Feb 2025 02:04:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd580f609e4457360db86df559c65d7e6f6e141b8169ff4f87fdb1afa978ddc1`  
		Last Modified: Thu, 06 Feb 2025 02:04:27 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432566dc815114577700fcfa9a2a02b50d92f00be3161bb3cb4533f85fd84c3`  
		Last Modified: Thu, 06 Feb 2025 02:04:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c4c0c2a267565fe7e2fdd8bb3d8d8d76a39815aed01dd9961642d3d98a877`  
		Last Modified: Thu, 06 Feb 2025 02:04:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b3861d657feb076ad01a5f3e2eebd3b8e5aac7131f089c94a4c2f32b1ff70`  
		Last Modified: Thu, 06 Feb 2025 02:04:41 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.3.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9c4ebb148d14f3fe4a1590cc5bb70caf6556717b00be0b26effaee422b4baa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c62d200dcf8a6f37d671db34fe9542b48a4a31646d494ad55589803abcc6d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f9b4c34cbe87a85d210676c8030e73d3a2e5b1343fc89067d1655ad26c52e38`  
		Last Modified: Thu, 06 Feb 2025 02:04:49 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12-jammy`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.3`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.3-jammy`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.3.47`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.3.47` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3.47` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.3.47` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3.47` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.3.47-jammy`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.3.47-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3.47-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.3.47-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.3.47-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3-focal`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.15`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.15` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.15` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.15-focal`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.15-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.15-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.15.72`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.15.72` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15.72` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.15.72` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15.72` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.15.72-focal`

```console
$ docker pull clickhouse@sha256:7db39c9f0fc59c8440c41c55ec1bf73765e4103ed7265b56ee192c80f97bc538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.15.72-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e1ee798d75feeac58229212e5ff11594a05dc366e6d98e5a248ddfeea551dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297482603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843b6ed21280054312fbad7450e09122c4207017e84391e53a1186f8f7d0b24`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7860681b8d78f0b46c1cfcb1f9caca1326102a00292e338b003d9a32aa8f5f`  
		Last Modified: Wed, 05 Feb 2025 08:11:12 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464d6ef30c4f92b5c82d4a026a861d50938fa5d9503f3eff0c7e37ef46ceddd`  
		Last Modified: Mon, 10 Feb 2025 05:30:44 GMT  
		Size: 260.3 MB (260301509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8fcf39d8d8b4e52b1ec59fe1322dc3ab92b569c439667f6a8227ae13c8827`  
		Last Modified: Fri, 07 Feb 2025 07:55:43 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653f5aaafe9d2b035aeda1abcb8797604bc3244490e21f2b378fcdfe7c74c71b`  
		Last Modified: Wed, 05 Feb 2025 08:19:09 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097d4e22ca668883ff82c17afad147aaad4e47940512ba2c811dff8e82556d4`  
		Last Modified: Thu, 13 Feb 2025 01:53:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340117141ab084d900655f6d6cc8324498fa29220c56e8bb63a62f2389a41bf`  
		Last Modified: Mon, 10 Feb 2025 05:30:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72b1a8dfe80dc7821260046470fe70a27136377ea3d7e2732876c452a04b1`  
		Last Modified: Thu, 13 Feb 2025 01:53:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15.72-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2df200b1858a3311f5cc3e1db96c7ce739a5ab16d25eaa47e18d4ba9d73bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5664d02cee2c14f136713b37b0cad1a4c844f219a0688bb6ae6b7508dc6f99`

```dockerfile
```

-	Layers:
	-	`sha256:7798f2de0d5141ed60829d3b2cc8994aa573370f6eb3b1109d17359c4103f4ee`  
		Last Modified: Wed, 15 Jan 2025 22:29:59 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.15.72-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:bb8d3af2190f776ab949f99e20b4c1fc4ed166b8054371042e6fe78b520d5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286065291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aecf3a52d58862afead8b436273d2b76f31f11fd7219490d9a2b3707c599e2`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.3.15.72
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.15.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb6d1512d48b2a602b6e4637802a6f10fb196252657dcf9dfbddc588709789`  
		Last Modified: Wed, 15 Jan 2025 22:35:53 GMT  
		Size: 250.6 MB (250561711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13048d88b5acfd51b6528dc1668901df1b62c3ec5c45126e77d58c9dc105bd2e`  
		Last Modified: Wed, 05 Feb 2025 08:10:31 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec0f7f6fbe33fc3200a0eea4d7c84f0c0013279366537e1c03f0253f26c584f`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641090067bb446f04e09428a3dc420e3d42e35aff07267723bb45de69c1785b`  
		Last Modified: Wed, 15 Jan 2025 22:35:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc26db011e7082296c20eef3c482503750c6e19f5486b828176240fb611b34`  
		Last Modified: Wed, 05 Feb 2025 08:10:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913cfc3871ed7fb6cb7e1b864ee149956658d6a0aa7cb61121ad7ecb286bc2a`  
		Last Modified: Wed, 15 Jan 2025 22:35:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.15.72-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b82850c4860080fbb04f463cb0fceb5cc913e6a4572b392d754f0acda593899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49299df1089d212658069ab8d1fd96402e0386ec33f5dcaff463181fd130630e`

```dockerfile
```

-	Layers:
	-	`sha256:1f33c8c8b62219763465b58fc7b159e51683639b72cabae64595c5e3cea8390d`  
		Last Modified: Wed, 05 Feb 2025 08:11:23 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.12`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.12-focal`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.12-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.12-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.12.28`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.12.28` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12.28` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.12.28` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12.28` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.12.28-focal`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.12.28-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12.28-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.12.28-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.12.28-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-focal`

```console
$ docker pull clickhouse@sha256:bebb8b88f00145151b9b4b114f86f49dab6094604ac77f52ebbb2a180ee7a5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:f7192ac051360ae08db75d330e3107b0f97c504225b4ac32f73f471c268fe20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda00b10363ddf657a353430202d107334791dc0c609150f3e1d4a09b6694cd`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7a388f1f0ee4312ac03ad06b868b65b8f2f5b58c7b3e6867ef77897497706`  
		Last Modified: Tue, 04 Feb 2025 13:40:26 GMT  
		Size: 8.8 MB (8802746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1eb049310760204e7b82e60db1ff05770959b33c1a6833544f0cf040cf5af3`  
		Last Modified: Tue, 04 Feb 2025 15:39:08 GMT  
		Size: 141.7 MB (141687501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd24e307619bac6c7f8c93e5e89c383afbdc63581166c44a71d19f2b15017b59`  
		Last Modified: Wed, 05 Feb 2025 13:13:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5ea881ba656f0250a083011043de821c4e91ae1a2373503e4faccd97ecf06`  
		Last Modified: Wed, 05 Feb 2025 17:54:30 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7275feab896f018d4ef3a42d3cbb79968f4921deee3d0607b75b1338fa243ca0`  
		Last Modified: Wed, 05 Feb 2025 09:31:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b249f2e1f3af7425aa00be8fc81f3aeac0b91be57edef4d7ed2862c72dc78c2`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793b6249eba5c9dab49f93f7235b15b0789d381b8122043d0a44c901d60b3ed`  
		Last Modified: Tue, 04 Feb 2025 15:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:33ff7f9df50645e8f8c6eb9737060b5384f09d9d2b56a2c9e9cdb4485772dcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9863009e79f2566da6357a637b5a7159ff029b92dd350a54f3ba818f5f91845`

```dockerfile
```

-	Layers:
	-	`sha256:b2373ce5ac37a587c86efe4f3504146bc61e005644ada4fff10a873cc3103479`  
		Last Modified: Wed, 05 Feb 2025 09:31:18 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:06836eb57e132067e2b6844a06e3a58b3534048763c8a0e54eec70fa6d4479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172238873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbee134b4c8aca891969ecd9cf32ac47cc030255d8343286232ac34c8a134ea`
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
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.8.12.28
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.12.28 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a413031e188f5c945d7dadccf53f46493e4a9ccfa83aa92c6ce61877a95d79e`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 8.7 MB (8662315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adff3e98de21628e3c557f00ea289ed3901572b4fbc6a87d47950b6e098c15`  
		Last Modified: Thu, 06 Feb 2025 03:35:39 GMT  
		Size: 136.7 MB (136735447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f75636cb3c429b5277fe891bdb3f12c2f519c39d77cc04cd4988ff57e0f0f`  
		Last Modified: Wed, 05 Feb 2025 09:31:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6bf416cf129f35390492098951557cb198f60d694af61dfcea52e651e89b2`  
		Last Modified: Wed, 05 Feb 2025 09:31:22 GMT  
		Size: 863.5 KB (863475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cffede79ceb52fd0b509c01ae2f2334a8f8a06bf4ac9ba49495a0727e4ec59a`  
		Last Modified: Thu, 06 Feb 2025 03:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b9b862d3bc81291f516c08a835baf33d60f646792550dbb08835fe6e5d273`  
		Last Modified: Wed, 05 Feb 2025 09:55:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf5ff181f079ad493ee8a696a3f988b79b14199acd17d3c9394ebccad235ed`  
		Last Modified: Wed, 05 Feb 2025 09:55:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dc29e2008c7bbd3887e06a2cc29162145c2260da90a15ec7458f512dd2dcd63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a6050966f649fb4cf657ecdd68943ea2c4559c16fa51b0cca9f1b5ab8a142e`

```dockerfile
```

-	Layers:
	-	`sha256:52fa9ca12ace344d25dd1856dcf2951da8605dfe1e4dc5330fe0517310eefa55`  
		Last Modified: Fri, 14 Feb 2025 01:39:31 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json
