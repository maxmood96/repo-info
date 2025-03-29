<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.14`](#clickhouse24814)
-	[`clickhouse:24.8.14-focal`](#clickhouse24814-focal)
-	[`clickhouse:24.8.14.39`](#clickhouse2481439)
-	[`clickhouse:24.8.14.39-focal`](#clickhouse2481439-focal)
-	[`clickhouse:25.1`](#clickhouse251)
-	[`clickhouse:25.1-jammy`](#clickhouse251-jammy)
-	[`clickhouse:25.1.8`](#clickhouse2518)
-	[`clickhouse:25.1.8-jammy`](#clickhouse2518-jammy)
-	[`clickhouse:25.1.8.25`](#clickhouse251825)
-	[`clickhouse:25.1.8.25-jammy`](#clickhouse251825-jammy)
-	[`clickhouse:25.2`](#clickhouse252)
-	[`clickhouse:25.2-jammy`](#clickhouse252-jammy)
-	[`clickhouse:25.2.2`](#clickhouse2522)
-	[`clickhouse:25.2.2-jammy`](#clickhouse2522-jammy)
-	[`clickhouse:25.2.2.39`](#clickhouse252239)
-	[`clickhouse:25.2.2.39-jammy`](#clickhouse252239-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.2`](#clickhouse2532)
-	[`clickhouse:25.3.2-jammy`](#clickhouse2532-jammy)
-	[`clickhouse:25.3.2.39`](#clickhouse253239)
-	[`clickhouse:25.3.2.39-jammy`](#clickhouse253239-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 00:27:43 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:27:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 00:27:41 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14.39-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1-jammy`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8-jammy`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8.25`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8.25` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8.25` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8.25-jammy`

```console
$ docker pull clickhouse@sha256:dab2090cf364d778e8fae06de6eb4fcc4afc4392e876756ef3f98f7913b32306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8.25-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d222992ec3ab91ec5b161d6bb1f8831e744529d7ea83cd6ea170ddfd0266b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191115849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145a9f2634103b5a134932700a94025eb73b0b3703c4328be4812923540702f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01589a5d9ad5915199c4308aa2ee86e1e88c643c634ed0801025af43dc2650cf`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 7.1 MB (7146951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad01766ca50ccd5a578200eccf4e28f9bcbd750b745216741e0345d90ed3d3`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 153.6 MB (153562704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e066ef9c25fb66383779904ec6976eda8ffbaf7fbc9e0cb5d8b1a674bb1601`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8408e6d45b008e918023cfb5c9b41b3b55f255e69b348848209357132614c`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4543c6044d857182483cf769a276eb55f2c19c9885bff6010f7822dc5755a565`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59d4ddab974453af3de5d1e6e52b62599aee6c1fa64d0639ed6bd61e36959c`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270316f2041f2ca2496e8e1a85f116effba6c9674a7c741c1178ecad95815e3`  
		Last Modified: Tue, 18 Mar 2025 18:01:55 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:91541e34724527e637990889d3e184c1f0369d9620d8cfcde69bef1fef993b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476082b255bc2c296c7b6091cbebbac9525942ecbfba6d3dbc5c0ef03e4de792`

```dockerfile
```

-	Layers:
	-	`sha256:234a3c6472667bdbd68a0edad156e8ee74dd0fa05477f91aea5841985ca00265`  
		Last Modified: Tue, 18 Mar 2025 18:01:54 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8.25-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2-jammy`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2-jammy`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39-jammy`

```console
$ docker pull clickhouse@sha256:57879229fca77f6892996be7824661ffaea83b8472a5368bfd9aead2de74856f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2-jammy`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2.39`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2.39-jammy`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2.39-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2.39-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:2d9baff31c0471aa18c9434af61c0e64107060f955dd90044c2a17eaabefcd4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1d98031d71cf468caaaf3c0aafe08dbaa42c23623b98f3909f2b496805ee7df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204545181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722360a96e522d39604f2df8c8831797c0facd64557635d5a065fdccbfab8bc6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033892b04edfda012fcbd3785430cfd6e6925e9fef37ed6f6f30a59de808f19`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7147251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbbb11962a02221afd59b2f3a3c4dde61a4235ab29f5b7bd1c354190f5cfdf`  
		Last Modified: Fri, 28 Mar 2025 21:06:11 GMT  
		Size: 167.0 MB (166991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d063dea497059c813e4c40590259d151797e3cff52d9a9240628852717751e`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a8a41306babc6a66948f8fa05b099d7b657aca7e0ae7cf4bbd1fbc9871311`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48863b550adaa1d3bd0534eade6e172a384ae0970620dd0cd63ac0625324f2f`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57c416608d9658e45aab8ee338032a311a22aaf60292cdb915c81fcb6bee0d9`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:839b7eabafe53829531cd1a79d2a8b44b2038799bea176ab4ada7d0d2843d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d0df2e9ac6fdde364b6a6b8d4f0109c29bf4d99877283fb15e4b099cf384b`

```dockerfile
```

-	Layers:
	-	`sha256:39588f2a7804ec734147f0008af6fcc32a6a0b80d8053e3b6ea413d6d367575b`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json
