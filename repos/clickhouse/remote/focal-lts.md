## `clickhouse:focal-lts`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:focal-lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
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
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal-lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:focal-lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
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
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal-lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
