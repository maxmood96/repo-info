<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.8`](#clickhouse25128)
-	[`clickhouse:25.12.8-jammy`](#clickhouse25128-jammy)
-	[`clickhouse:25.12.8.9`](#clickhouse251289)
-	[`clickhouse:25.12.8.9-jammy`](#clickhouse251289-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.14`](#clickhouse25314)
-	[`clickhouse:25.3.14-jammy`](#clickhouse25314-jammy)
-	[`clickhouse:25.3.14.14`](#clickhouse2531414)
-	[`clickhouse:25.3.14.14-jammy`](#clickhouse2531414-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.18`](#clickhouse25818)
-	[`clickhouse:25.8.18-jammy`](#clickhouse25818-jammy)
-	[`clickhouse:25.8.18.1`](#clickhouse258181)
-	[`clickhouse:25.8.18.1-jammy`](#clickhouse258181-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.4`](#clickhouse2614)
-	[`clickhouse:26.1.4-jammy`](#clickhouse2614-jammy)
-	[`clickhouse:26.1.4.35`](#clickhouse261435)
-	[`clickhouse:26.1.4.35-jammy`](#clickhouse261435-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.4`](#clickhouse2624)
-	[`clickhouse:26.2.4-jammy`](#clickhouse2624-jammy)
-	[`clickhouse:26.2.4.23`](#clickhouse262423)
-	[`clickhouse:26.2.4.23-jammy`](#clickhouse262423-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8-jammy`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8.9`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8.9-jammy`

```console
$ docker pull clickhouse@sha256:392508924677e4203eba4f0c54eafb859222508855a40d9e2036b1ae3f9addc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:18c069cfc7ef9e2e5827f328236201606efd3da2b46a1642039cea02ec18203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228293360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8aab7f9808d3f969a6736ceb886fa3a05766ea313b61132c171c5cbcab770a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:33 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf7641869cab040128427994bbb326d593ef823a438a39e6fbe65f1c62544f`  
		Last Modified: Fri, 06 Mar 2026 18:23:56 GMT  
		Size: 192.5 MB (192460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d96f1d090a8b185c75121554b08f49a5aa7ae45ad48209c2adeb1012a5ff9`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104ca7dfa25b650e8ba8d0b23c66909fc52d991bb0c54fdca5ffe79885dcba98`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785a568c300dce24089a56ac240d922bcad483ecf0ef57e0469135ca6f7bb254`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12603a65872019dba8d92beb8eb8e373948bddd9ee03b7269d46aae4f1571617`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa6e949a0ff3f7aff6fd06902ae17e15fc9b77ad87836a3ed62318ccfee9fa`  
		Last Modified: Fri, 06 Mar 2026 18:23:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5a61ec4cfcf0081c730991b7c39d25c649c24eb49db30fa62f7cf03271fd46b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8345e4fb5cacbd80fe98f146f21823ffa45b598a70ed88a0064b1388df2ad1`

```dockerfile
```

-	Layers:
	-	`sha256:da6dee4c72500ef4b868c87e82ddb8a746402767a5d26650a96836da6d23c91c`  
		Last Modified: Fri, 06 Mar 2026 18:23:52 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18-jammy`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18.1`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18.1-jammy`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4-jammy`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4.35`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4.35` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4.35` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4.35-jammy`

```console
$ docker pull clickhouse@sha256:16e9f1389e85100b2b0791805526d2cfb4a2bb699647952b24253b00d1ee4c9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4.35-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4.35-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:88612d0b4efd5fbc468e5ee14e18980640c50a6b6a715aa51cdbdc9a056f324b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228243118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a481c945ce555aa8cf23195a3e738ccdfe32e2fd51e453cbe807c0e97f9ddab4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:04 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:22:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:22:31 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:22:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:22:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:22:31 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:22:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19d12cb279feb3f05923f73020404576eba041e54f1ec70ac1a2c49b828703`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 7.6 MB (7577559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48101163b7107d38196096eeb6c23768a3e83e1ba26162eb606269859741b51`  
		Last Modified: Fri, 06 Mar 2026 18:22:58 GMT  
		Size: 192.4 MB (192410572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d761805ec46925c5166c2bad4b38de52cfc24dd297610d07201d2050d0272c`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d3c4adcf91f50571836304865e92e73ea28dd615dfc30ce828073c3fcb4fd7`  
		Last Modified: Fri, 06 Mar 2026 18:22:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192354ea1fff932a94829f542c1e94d9fc380fd8a973cfa3fe5e011f3ecf5843`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa8c6c133c8267c28c0bd28b6f41f5c98222b961ebc56e6638de542459fea0`  
		Last Modified: Fri, 06 Mar 2026 18:22:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db920424ce2448a843b037ea653cbaf9a5e61176a5248a67954896fb1d4a7b54`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4ab9e132119460d5cc5eba467ef45f4781a35857420504f2629190e3cb033516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49330bd39f9630c3b3c742e02582669c7a959d4a4ee6633f7f2821912ebef125`

```dockerfile
```

-	Layers:
	-	`sha256:09dbf402a3694f1a9275422a0f593af7d3169de16e29fcb88ce2f8a1c9253efb`  
		Last Modified: Fri, 06 Mar 2026 18:22:50 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4-jammy`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4.23`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4.23` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4.23-jammy`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4.23-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:abee8a782fa62d92b8eba945097b3ff97bf2ab1b98fe4da8c91632101f184bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:727759fcaa684438aedfc858833878761a745029cfca8f49f16b5c4a792e1e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237152519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e8d072807c87df4787c86e1ac35429b496d887985c3ea0032ceaca495d7b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:23:23 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:23:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:23:23 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:23:23 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:23:23 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:23:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac05fca3f846594fbb2c4091c89d3ffcedf5349c21f466f0e1a54e9c0710e10`  
		Last Modified: Fri, 06 Mar 2026 18:23:49 GMT  
		Size: 201.3 MB (201319972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4054a129dfc7f8bea1c94d4c42aed5a7225f519b9e874a621f050784e26608`  
		Last Modified: Fri, 06 Mar 2026 18:23:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13d354d75d7183a6f3a5847ce11ea6767aa93091d576e4a38030c04c61333c1`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e93a59d4615f84ecaaaea0518d26a61f58cc156186d64986517cb56426659`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf60cfe8553db51d751647507eb13581f8fbc152e145bbbad42afe0547e1139`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728acdb15f1b547cf9dc9ded1500196bac22c1aafff057a24bbb312a1ebfade7`  
		Last Modified: Fri, 06 Mar 2026 18:23:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2d97b1d0be6edc2ce351690c94d3d4fd72e29a1b8d0ebb127b9f89b4d72a075f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2401c9c5d03862fdc452263e8570a8ff44c080ba819b41c034a9d365d96d03d`

```dockerfile
```

-	Layers:
	-	`sha256:15056dab38957634dba042a164e501ea0d56403bfd5b4e5520f189af11993402`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:8c4e9520a0734e1b1d88c91c51bcead9522a3b23b108fedf09394697777adda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:3018a35989f6ce8214f161ff4a45286a94d12dfccf59e13f58ba02b6aee21376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9798c9eb00f3737eec5ac306ba668bb07ce79f1f923288cf524c8eb39af24f3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:22:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:22:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:22:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:22:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:22:50 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:22:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:24:24 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:24:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:24:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:24:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:24:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962b006aa9faa9d43414117d8cddc9ac4091a70797cc49c85c38e5573dccad4`  
		Last Modified: Fri, 06 Mar 2026 18:23:45 GMT  
		Size: 7.6 MB (7577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4df00eafad6e780faeaa03f2ad1a384664a3031257784088e3b0ace854f69`  
		Last Modified: Fri, 06 Mar 2026 18:24:46 GMT  
		Size: 178.0 MB (178015841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e75c97bd33a252fb197ccd81783f3e5fffcd0b0a2edf65b35792f9532d6b2`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd40dcc718604a906d7c55c17ed938f531b229494b7e7104dd8af2388c2dac`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896291bf27190645aef84bb5cd0dacd17841f8ea9dd353b58c296cff939f175`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f2bd4cc76429de0cc3b0629dedb2c89af655bccd12a62d3fa92c6c4f91a886`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf28972dcac1e042f402da2b7c7610dfc24e3ad0e6acd0223c791b966f6e78`  
		Last Modified: Fri, 06 Mar 2026 18:24:43 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6a930479175af80fb71311422b1b48a8a43461e4fafd8690db8f142d88e664e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0867dc1957c88413d8124f637224c1cefdf2169acc187321bd538d30b00a9e1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c25daf4f176d6f536e4f7becda45b46e17031e1e37c0d45d40e1318ea612c`  
		Last Modified: Fri, 06 Mar 2026 18:24:42 GMT  
		Size: 26.2 KB (26246 bytes)  
		MIME: application/vnd.in-toto+json
