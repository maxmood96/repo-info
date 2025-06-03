## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:668cf02c7d67eaafb8f3e4614f7a8d24caf05130acf551616b887401ad89ea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:4643fe917573fe06f4c8dd4dfadef5d3ebe7151ed4b96f611c61d763e3748ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e032593a9b1d712a6691d4dd875ee034429aee64aee1378d602f1a05ba54c26`
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
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:ca18d4ea7ff898eccbdea1b99a52ed6bdaaea18e98a4bf7af4ca5bfaa621ec23`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 7.2 MB (7151670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48829f4421d0dc1bbbd6afcd428c3faec27c484876b236ac7e8a8c4ee51baf8`  
		Last Modified: Tue, 03 Jun 2025 13:34:21 GMT  
		Size: 168.4 MB (168437610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811205cc2b9315b293d4e880a8ad4f5754d52b97b914a8f6352f95ea6622eaf`  
		Last Modified: Tue, 03 Jun 2025 13:34:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6534354a8849b34990c5ed5890969dc652fbfa136ab05e4cefab0f590b1d4078`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379441ad211fd0d8c6ec812815a3b8606491121410986aae2b00ea51d5044a0c`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5d8424dd133095c22862d02ae4f4c94fe85e8fce55a80ff81dc361f046852`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944eae3ea89105f619ac2cfb8c646ec888c46cf07833e2ce12e0358eb0837e01`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:02aedb60d80131305dfb8d4b1b8218e2679c1d37d9abf20a1fefd4901f96534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d838c21a4277e4e8ea3a128d2819b0df050fd16d96ed68af5a11fe8f943c09`

```dockerfile
```

-	Layers:
	-	`sha256:edc7d8f4736b9ae1f52da66199f68cf486442ffe98e72122d2db61909ac143f4`  
		Last Modified: Tue, 03 Jun 2025 04:16:24 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d9ddfa0947aecce3ff098371cdfeae355a9b7d08de5eeccdca15d2b37ba8172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192488684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedafce23b87a9ea7f6f39756bfc693a5da8c391d2935f2bf98e5d1931c12d1`
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
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:78c5b38a39c18549c81527aeb48892dfc585c974a9a93e66ca884ef8f820e0bb`  
		Last Modified: Tue, 03 Jun 2025 04:21:44 GMT  
		Size: 7.1 MB (7127793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e8d6308303920e9c697de9ede1387bdd197d6956d6a41ac8842e7bfb5bd75`  
		Last Modified: Tue, 03 Jun 2025 04:21:47 GMT  
		Size: 157.1 MB (157135063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c044a90340fc36e81cc8e57c8142c9c4c66b59009d6db03191c5164689db72`  
		Last Modified: Tue, 03 Jun 2025 04:21:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c3a68ef15e5229ad768ec84c430df2eeea6f52d92a20a184feac13be30294`  
		Last Modified: Tue, 03 Jun 2025 04:21:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376439689a943599fdeba7d8d47b32eb05623a1a107d3d581a024b2667b427de`  
		Last Modified: Tue, 03 Jun 2025 04:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae75e427a60ab183d457bb0286429b0156fde1596cf3cfa4cffaab4e866f02`  
		Last Modified: Tue, 03 Jun 2025 04:21:45 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb5196123393dcbeae3363eea4352814819c479b7bea9f0c824b8b7ac96ab`  
		Last Modified: Tue, 03 Jun 2025 04:21:45 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ab474a83ef83d13412e1c671e86e3ece02eefedf10ef94cde070bf4fcdef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24c0ce6ab07378dc1724d7f5a76f1233cc852b02d6941a6aa8ccc14cfdb383`

```dockerfile
```

-	Layers:
	-	`sha256:a3df743e65c02fd92d1afe55481b59d7a2399accd6e3c326d22f2b3ce101c60f`  
		Last Modified: Tue, 03 Jun 2025 04:21:43 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json
