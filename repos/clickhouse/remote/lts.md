## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
