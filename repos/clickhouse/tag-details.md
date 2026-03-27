<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.20`](#clickhouse25820)
-	[`clickhouse:25.8.20-jammy`](#clickhouse25820-jammy)
-	[`clickhouse:25.8.20.4`](#clickhouse258204)
-	[`clickhouse:25.8.20.4-jammy`](#clickhouse258204-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.6`](#clickhouse2616)
-	[`clickhouse:26.1.6-jammy`](#clickhouse2616-jammy)
-	[`clickhouse:26.1.6.6`](#clickhouse26166)
-	[`clickhouse:26.1.6.6-jammy`](#clickhouse26166-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.5`](#clickhouse2625)
-	[`clickhouse:26.2.5-jammy`](#clickhouse2625-jammy)
-	[`clickhouse:26.2.5.45`](#clickhouse262545)
-	[`clickhouse:26.2.5.45-jammy`](#clickhouse262545-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.1`](#clickhouse2631)
-	[`clickhouse:26.3.1-jammy`](#clickhouse2631-jammy)
-	[`clickhouse:26.3.1.896`](#clickhouse2631896)
-	[`clickhouse:26.3.1.896-jammy`](#clickhouse2631896-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:85f5e737d998396332012c0ddb796330448c50bb4f0d567ea161dbbd7b80d71d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:9088f4d2cba1fc8d198d72a152906ab82bc6ac2e07ac9cb6bf0b1c3ca2fa6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228957865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8122f8f5c497b5b6edd03f01d9c1d75d9553664a45dfe554806d6cc539d0fcfd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:21 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:21 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:21 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:21 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:51 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:52 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af4761fa94bb2fb779f2b2a0d5b26af6c5f89f1fd5e5fa2f088fe8fd49c0d8`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 7.6 MB (7598298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bdada8c4ee2383f3495d6043ade0d7cd9dec1a9f36597df68babb5143c4e1`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 191.0 MB (190951023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d3b469e944891b8d52ffc19b1bf6cee9dbd8b740f9070127b3c5a755c196a7`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d08a9c2d825689cde410c48cd7aab966e85ede9b3e45ef6000e7fc084f7fd89`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e73f1d963988f03ebbdfc8ee1a885801b4b910f8b1206d749c8a6fe65cfaa79`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7887e7a237042c6b52ae1a6245a911550f2128613029582cfe72aa0801be54a`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ce7773c0b10f3fe77d5f2cb808a5c1c19956b498a258b65648c3f96c9462f`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aa81c22da1268f2c6eb643d7d3ba9c7acfd95328b7130e966f1cdf577f841552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2918c7a363b0fec43a22cf68dc2162640f902c2b9d9d0b2b480552b4a1b160b`

```dockerfile
```

-	Layers:
	-	`sha256:1322a7eccbf4caaaefab9daa764f5888f89e885d6131c4826549d610850856de`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:85f5e737d998396332012c0ddb796330448c50bb4f0d567ea161dbbd7b80d71d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9088f4d2cba1fc8d198d72a152906ab82bc6ac2e07ac9cb6bf0b1c3ca2fa6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228957865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8122f8f5c497b5b6edd03f01d9c1d75d9553664a45dfe554806d6cc539d0fcfd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:21 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:21 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:21 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:21 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:51 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:52 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af4761fa94bb2fb779f2b2a0d5b26af6c5f89f1fd5e5fa2f088fe8fd49c0d8`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 7.6 MB (7598298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bdada8c4ee2383f3495d6043ade0d7cd9dec1a9f36597df68babb5143c4e1`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 191.0 MB (190951023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d3b469e944891b8d52ffc19b1bf6cee9dbd8b740f9070127b3c5a755c196a7`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d08a9c2d825689cde410c48cd7aab966e85ede9b3e45ef6000e7fc084f7fd89`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e73f1d963988f03ebbdfc8ee1a885801b4b910f8b1206d749c8a6fe65cfaa79`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7887e7a237042c6b52ae1a6245a911550f2128613029582cfe72aa0801be54a`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ce7773c0b10f3fe77d5f2cb808a5c1c19956b498a258b65648c3f96c9462f`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aa81c22da1268f2c6eb643d7d3ba9c7acfd95328b7130e966f1cdf577f841552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2918c7a363b0fec43a22cf68dc2162640f902c2b9d9d0b2b480552b4a1b160b`

```dockerfile
```

-	Layers:
	-	`sha256:1322a7eccbf4caaaefab9daa764f5888f89e885d6131c4826549d610850856de`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20`

**does not exist** (yet?)

## `clickhouse:25.8.20-jammy`

**does not exist** (yet?)

## `clickhouse:25.8.20.4`

**does not exist** (yet?)

## `clickhouse:25.8.20.4-jammy`

**does not exist** (yet?)

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:93d8d84765899b7a0ee9d1b3c7ecebc639ac6d11e5825ae1205ce000e8e7c2c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:870728cf147eeed1fd336cad048e6d4addf7d134c32a9ee6be44e13c4b2069e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246002725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28195089cf54db0577af8bdef10f95b2c5480759314b78901549033c51d8e361`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:34 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:03 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29539ad59bc616964130407f929b14c680246f7c3ad23b48eac8285e52f82f29`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 7.6 MB (7598319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9004f6ea21b5e8fcc989f8741a533156505cb4c7295cebc5b3a7ac52b224f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 208.0 MB (207995835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04723e6fb11b678404a1ef0aa8356257a4ad89476dfbecb8ffdc82f5b0654133`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee06e098af3b19f483a1fcbe236995060b84fda072313e8db15126785d0a325e`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dcfb9838a52b0ed55ebaa73f1e01e79dd311745f62c012d6e0a99fd1a6d616`  
		Last Modified: Tue, 17 Mar 2026 01:16:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f330a32190dad0e396f9ef64989f7f82fa83a2f6b7d87fdbe0f187660c49209a`  
		Last Modified: Tue, 17 Mar 2026 01:16:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd19b87999305bea8adbd53d2abfbd52b61916905dfe617f312f3ccb82761cd6`  
		Last Modified: Tue, 17 Mar 2026 01:16:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f0d31831892696494be9ef673b00aa62f3e8aeaffff5368f9424bf4fbfe78136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d026cf25d6818f4398eade0291b09a8f40452e5ab8cfbcbb54ddb057993f02`

```dockerfile
```

-	Layers:
	-	`sha256:08267422f4af502bcaf3466cf54e7d8facf0921fab4e7b3a923edd198c529c25`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:93d8d84765899b7a0ee9d1b3c7ecebc639ac6d11e5825ae1205ce000e8e7c2c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:870728cf147eeed1fd336cad048e6d4addf7d134c32a9ee6be44e13c4b2069e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246002725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28195089cf54db0577af8bdef10f95b2c5480759314b78901549033c51d8e361`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:34 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:03 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29539ad59bc616964130407f929b14c680246f7c3ad23b48eac8285e52f82f29`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 7.6 MB (7598319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9004f6ea21b5e8fcc989f8741a533156505cb4c7295cebc5b3a7ac52b224f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 208.0 MB (207995835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04723e6fb11b678404a1ef0aa8356257a4ad89476dfbecb8ffdc82f5b0654133`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee06e098af3b19f483a1fcbe236995060b84fda072313e8db15126785d0a325e`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dcfb9838a52b0ed55ebaa73f1e01e79dd311745f62c012d6e0a99fd1a6d616`  
		Last Modified: Tue, 17 Mar 2026 01:16:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f330a32190dad0e396f9ef64989f7f82fa83a2f6b7d87fdbe0f187660c49209a`  
		Last Modified: Tue, 17 Mar 2026 01:16:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd19b87999305bea8adbd53d2abfbd52b61916905dfe617f312f3ccb82761cd6`  
		Last Modified: Tue, 17 Mar 2026 01:16:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f0d31831892696494be9ef673b00aa62f3e8aeaffff5368f9424bf4fbfe78136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d026cf25d6818f4398eade0291b09a8f40452e5ab8cfbcbb54ddb057993f02`

```dockerfile
```

-	Layers:
	-	`sha256:08267422f4af502bcaf3466cf54e7d8facf0921fab4e7b3a923edd198c529c25`  
		Last Modified: Tue, 17 Mar 2026 01:16:25 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6`

**does not exist** (yet?)

## `clickhouse:26.1.6-jammy`

**does not exist** (yet?)

## `clickhouse:26.1.6.6`

**does not exist** (yet?)

## `clickhouse:26.1.6.6-jammy`

**does not exist** (yet?)

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:39589ad7a73780ddeed8cb41dadf75c6f633c8d98c0b814e91b326e41353b976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:2910ae39f0166a853c421765faed05d86189ae4c020cd47a053c2b789ea140aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253566555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff506fc10c8ac7c90fb7b53c8732c5db55a0243b709f53a93621241e49cbe1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:19 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44a514f64a5c81b68d38250c3503257e4694cffa5a02a54ae54a825e3072b`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 7.6 MB (7598323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6e404823334f672a9a272d6c31d182c38397dcf93395ea6ed82e135fec616`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 215.6 MB (215559657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f3a14b1e7280c8dd6097eed134bf5e9b91ff731fb0ea21c3fdfea59417ffa`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b46c7dcea29f43f7b37733e49191779425f625922c21f10d7b0a9b6fbf78f1`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56906e81306b4d638d929cdf9b4db1f1c37f97bbc80a79b3292f4d4b33bea7c5`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe000e07ce3fdc72704a45f5969994ad87ab2c548e9daea125c173d481817330`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d045d50c6f7d0b5c43b2b367697596bf27da02d58861f18e1f42693fde831c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce1affd280a1b80b085c58deaed869ed4f2128c76f1dd527bc726a92f3af4d`

```dockerfile
```

-	Layers:
	-	`sha256:2b54da9706c5dd9fb36a622f9b3a108e4ef6c087aa594a3ec182268f42453f89`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:39589ad7a73780ddeed8cb41dadf75c6f633c8d98c0b814e91b326e41353b976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2910ae39f0166a853c421765faed05d86189ae4c020cd47a053c2b789ea140aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253566555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff506fc10c8ac7c90fb7b53c8732c5db55a0243b709f53a93621241e49cbe1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:19 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44a514f64a5c81b68d38250c3503257e4694cffa5a02a54ae54a825e3072b`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 7.6 MB (7598323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6e404823334f672a9a272d6c31d182c38397dcf93395ea6ed82e135fec616`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 215.6 MB (215559657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f3a14b1e7280c8dd6097eed134bf5e9b91ff731fb0ea21c3fdfea59417ffa`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b46c7dcea29f43f7b37733e49191779425f625922c21f10d7b0a9b6fbf78f1`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56906e81306b4d638d929cdf9b4db1f1c37f97bbc80a79b3292f4d4b33bea7c5`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe000e07ce3fdc72704a45f5969994ad87ab2c548e9daea125c173d481817330`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d045d50c6f7d0b5c43b2b367697596bf27da02d58861f18e1f42693fde831c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce1affd280a1b80b085c58deaed869ed4f2128c76f1dd527bc726a92f3af4d`

```dockerfile
```

-	Layers:
	-	`sha256:2b54da9706c5dd9fb36a622f9b3a108e4ef6c087aa594a3ec182268f42453f89`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5`

**does not exist** (yet?)

## `clickhouse:26.2.5-jammy`

**does not exist** (yet?)

## `clickhouse:26.2.5.45`

**does not exist** (yet?)

## `clickhouse:26.2.5.45-jammy`

**does not exist** (yet?)

## `clickhouse:26.3`

**does not exist** (yet?)

## `clickhouse:26.3-jammy`

**does not exist** (yet?)

## `clickhouse:26.3.1`

**does not exist** (yet?)

## `clickhouse:26.3.1-jammy`

**does not exist** (yet?)

## `clickhouse:26.3.1.896`

**does not exist** (yet?)

## `clickhouse:26.3.1.896-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:39589ad7a73780ddeed8cb41dadf75c6f633c8d98c0b814e91b326e41353b976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2910ae39f0166a853c421765faed05d86189ae4c020cd47a053c2b789ea140aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253566555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff506fc10c8ac7c90fb7b53c8732c5db55a0243b709f53a93621241e49cbe1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:19 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44a514f64a5c81b68d38250c3503257e4694cffa5a02a54ae54a825e3072b`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 7.6 MB (7598323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6e404823334f672a9a272d6c31d182c38397dcf93395ea6ed82e135fec616`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 215.6 MB (215559657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f3a14b1e7280c8dd6097eed134bf5e9b91ff731fb0ea21c3fdfea59417ffa`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b46c7dcea29f43f7b37733e49191779425f625922c21f10d7b0a9b6fbf78f1`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56906e81306b4d638d929cdf9b4db1f1c37f97bbc80a79b3292f4d4b33bea7c5`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe000e07ce3fdc72704a45f5969994ad87ab2c548e9daea125c173d481817330`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d045d50c6f7d0b5c43b2b367697596bf27da02d58861f18e1f42693fde831c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce1affd280a1b80b085c58deaed869ed4f2128c76f1dd527bc726a92f3af4d`

```dockerfile
```

-	Layers:
	-	`sha256:2b54da9706c5dd9fb36a622f9b3a108e4ef6c087aa594a3ec182268f42453f89`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:39589ad7a73780ddeed8cb41dadf75c6f633c8d98c0b814e91b326e41353b976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:2910ae39f0166a853c421765faed05d86189ae4c020cd47a053c2b789ea140aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253566555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff506fc10c8ac7c90fb7b53c8732c5db55a0243b709f53a93621241e49cbe1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:19 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44a514f64a5c81b68d38250c3503257e4694cffa5a02a54ae54a825e3072b`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 7.6 MB (7598323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6e404823334f672a9a272d6c31d182c38397dcf93395ea6ed82e135fec616`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 215.6 MB (215559657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f3a14b1e7280c8dd6097eed134bf5e9b91ff731fb0ea21c3fdfea59417ffa`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b46c7dcea29f43f7b37733e49191779425f625922c21f10d7b0a9b6fbf78f1`  
		Last Modified: Tue, 17 Mar 2026 01:16:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56906e81306b4d638d929cdf9b4db1f1c37f97bbc80a79b3292f4d4b33bea7c5`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe000e07ce3fdc72704a45f5969994ad87ab2c548e9daea125c173d481817330`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d045d50c6f7d0b5c43b2b367697596bf27da02d58861f18e1f42693fde831c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce1affd280a1b80b085c58deaed869ed4f2128c76f1dd527bc726a92f3af4d`

```dockerfile
```

-	Layers:
	-	`sha256:2b54da9706c5dd9fb36a622f9b3a108e4ef6c087aa594a3ec182268f42453f89`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:85f5e737d998396332012c0ddb796330448c50bb4f0d567ea161dbbd7b80d71d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:9088f4d2cba1fc8d198d72a152906ab82bc6ac2e07ac9cb6bf0b1c3ca2fa6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228957865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8122f8f5c497b5b6edd03f01d9c1d75d9553664a45dfe554806d6cc539d0fcfd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:21 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:21 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:21 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:21 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:51 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:52 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af4761fa94bb2fb779f2b2a0d5b26af6c5f89f1fd5e5fa2f088fe8fd49c0d8`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 7.6 MB (7598298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bdada8c4ee2383f3495d6043ade0d7cd9dec1a9f36597df68babb5143c4e1`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 191.0 MB (190951023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d3b469e944891b8d52ffc19b1bf6cee9dbd8b740f9070127b3c5a755c196a7`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d08a9c2d825689cde410c48cd7aab966e85ede9b3e45ef6000e7fc084f7fd89`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e73f1d963988f03ebbdfc8ee1a885801b4b910f8b1206d749c8a6fe65cfaa79`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7887e7a237042c6b52ae1a6245a911550f2128613029582cfe72aa0801be54a`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ce7773c0b10f3fe77d5f2cb808a5c1c19956b498a258b65648c3f96c9462f`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aa81c22da1268f2c6eb643d7d3ba9c7acfd95328b7130e966f1cdf577f841552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2918c7a363b0fec43a22cf68dc2162640f902c2b9d9d0b2b480552b4a1b160b`

```dockerfile
```

-	Layers:
	-	`sha256:1322a7eccbf4caaaefab9daa764f5888f89e885d6131c4826549d610850856de`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:85f5e737d998396332012c0ddb796330448c50bb4f0d567ea161dbbd7b80d71d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9088f4d2cba1fc8d198d72a152906ab82bc6ac2e07ac9cb6bf0b1c3ca2fa6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228957865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8122f8f5c497b5b6edd03f01d9c1d75d9553664a45dfe554806d6cc539d0fcfd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:21 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:21 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:21 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:21 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:21 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:51 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:52 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af4761fa94bb2fb779f2b2a0d5b26af6c5f89f1fd5e5fa2f088fe8fd49c0d8`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 7.6 MB (7598298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bdada8c4ee2383f3495d6043ade0d7cd9dec1a9f36597df68babb5143c4e1`  
		Last Modified: Tue, 17 Mar 2026 01:16:17 GMT  
		Size: 191.0 MB (190951023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d3b469e944891b8d52ffc19b1bf6cee9dbd8b740f9070127b3c5a755c196a7`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d08a9c2d825689cde410c48cd7aab966e85ede9b3e45ef6000e7fc084f7fd89`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e73f1d963988f03ebbdfc8ee1a885801b4b910f8b1206d749c8a6fe65cfaa79`  
		Last Modified: Tue, 17 Mar 2026 01:16:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7887e7a237042c6b52ae1a6245a911550f2128613029582cfe72aa0801be54a`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ce7773c0b10f3fe77d5f2cb808a5c1c19956b498a258b65648c3f96c9462f`  
		Last Modified: Tue, 17 Mar 2026 01:16:15 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aa81c22da1268f2c6eb643d7d3ba9c7acfd95328b7130e966f1cdf577f841552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2918c7a363b0fec43a22cf68dc2162640f902c2b9d9d0b2b480552b4a1b160b`

```dockerfile
```

-	Layers:
	-	`sha256:1322a7eccbf4caaaefab9daa764f5888f89e885d6131c4826549d610850856de`  
		Last Modified: Tue, 17 Mar 2026 01:16:13 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json
