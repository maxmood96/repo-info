<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.10`](#clickhouse2510)
-	[`clickhouse:25.10-jammy`](#clickhouse2510-jammy)
-	[`clickhouse:25.10.4`](#clickhouse25104)
-	[`clickhouse:25.10.4-jammy`](#clickhouse25104-jammy)
-	[`clickhouse:25.10.4.104`](#clickhouse25104104)
-	[`clickhouse:25.10.4.104-jammy`](#clickhouse25104104-jammy)
-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.6`](#clickhouse25116)
-	[`clickhouse:25.11.6-jammy`](#clickhouse25116-jammy)
-	[`clickhouse:25.11.6.11`](#clickhouse2511611)
-	[`clickhouse:25.11.6.11-jammy`](#clickhouse2511611-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.2`](#clickhouse25122)
-	[`clickhouse:25.12.2-jammy`](#clickhouse25122-jammy)
-	[`clickhouse:25.12.2.54`](#clickhouse2512254)
-	[`clickhouse:25.12.2.54-jammy`](#clickhouse2512254-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.12`](#clickhouse25312)
-	[`clickhouse:25.3.12-jammy`](#clickhouse25312-jammy)
-	[`clickhouse:25.3.12.8`](#clickhouse253128)
-	[`clickhouse:25.3.12.8-jammy`](#clickhouse253128-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.14`](#clickhouse25814)
-	[`clickhouse:25.8.14-jammy`](#clickhouse25814-jammy)
-	[`clickhouse:25.8.14.17`](#clickhouse2581417)
-	[`clickhouse:25.8.14.17-jammy`](#clickhouse2581417-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.10`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae4a23179563607286515620f647b2559d1ea898179cc80617b4e244557ea4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232760170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebaef512b4359f155aa63d217e35c8c9e8ebc5ebcb500debc3244f4d4997cea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:38 GMT
ARG VERSION=25.10.3.100
# Mon, 01 Dec 2025 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:05 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:05 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276901473cae3318825ebd8a2c7b01ba136e74e3ef0d5760f9ad60eb4bdae52`  
		Last Modified: Mon, 01 Dec 2025 20:06:53 GMT  
		Size: 7.6 MB (7598515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcdd1a31d92d6a1d0865cf2958294b4186697e64654cb9d37d194efde903518`  
		Last Modified: Mon, 01 Dec 2025 22:50:24 GMT  
		Size: 194.8 MB (194754832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cb0f66f2ce7c1e6dd699730df5b1477c307bf976e94f9c05329c5322c5b431`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04913bca25e195366a3830bada211999e720a1a6093b576ea62209686bea6f4`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452b0da22ef61b1ed15e78d38a817cc3966260f7d78a64c2a28b05fce416995`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed15771250801f0c87551c23c1364b0314f7a8c3951e4b1219c6c6430507f59`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335c680e8b100a4e9a710c60ddfc0a6ecff1d4e0f2c08de8978c7915d101a310`  
		Last Modified: Mon, 01 Dec 2025 20:06:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30f8b00e0976ff412c0be0b1ae015a38b24a46bc78d3c6f5c69d6388c5649ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598ab8f111b05daa9c651148ecff824b69b4dbe320927dea8bb41ff396437d9b`

```dockerfile
```

-	Layers:
	-	`sha256:0b0983d95cd00fb76ad8247da181d9d5248f80fc69f73ac0c338ac4deeb2d7fa`  
		Last Modified: Mon, 01 Dec 2025 22:49:58 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a593463cbc3623f694ac1f939edee81480e2ece7ff61c23c08119cdffe649c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217281108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4744404b490acc86290091007a95de84ea7f68bf06f8af0baead268c76356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 20:04:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:47 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:47 GMT
ARG VERSION=25.10.3.100
# Mon, 01 Dec 2025 20:04:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:17 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:17 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:18 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d5618a252cc58692a14ff5beae75f2ff42fac7881b91e4de2f5832850c63e5`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 7.6 MB (7576744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca96168027ac3934ed3848a116652491fa0a1c01004f63a9f1b197b67d4730`  
		Last Modified: Mon, 01 Dec 2025 22:50:30 GMT  
		Size: 181.5 MB (181450461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c95d11ea9b11716c710608e661d8298430a7dacb4178bea098dae5a380f07`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9412d6c48064ce045f545be8ba9486305e9565e6f4836be74f7cf8b5053a202`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937ccd4d46c777769d56d07e11b6dc9858d51c33abea9edeb688fd237e2b557`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa56fab2fea4770d737655f82ddb959347a3052192fe1055a49720cfbcdd2f45`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d847816d33f078a5734f381fbd1ce4023e65189207167d11e70fa15fa2a70`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:17bd58911ae219d07beb472e5264efbaa7f280a47fd2c3594b990da1eba0d30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1d17051f76d7ab03fee2d81d1eb2cd2e8d2ee34ba890faee48e51593900f21`

```dockerfile
```

-	Layers:
	-	`sha256:91a08a09ef402d13bbdf7bcb2f87f925fef70df83a0cda20a6df42a16c3dff0b`  
		Last Modified: Mon, 01 Dec 2025 22:50:01 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10-jammy`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae4a23179563607286515620f647b2559d1ea898179cc80617b4e244557ea4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232760170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebaef512b4359f155aa63d217e35c8c9e8ebc5ebcb500debc3244f4d4997cea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:38 GMT
ARG VERSION=25.10.3.100
# Mon, 01 Dec 2025 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:05 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:05 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276901473cae3318825ebd8a2c7b01ba136e74e3ef0d5760f9ad60eb4bdae52`  
		Last Modified: Mon, 01 Dec 2025 20:06:53 GMT  
		Size: 7.6 MB (7598515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcdd1a31d92d6a1d0865cf2958294b4186697e64654cb9d37d194efde903518`  
		Last Modified: Mon, 01 Dec 2025 22:50:24 GMT  
		Size: 194.8 MB (194754832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cb0f66f2ce7c1e6dd699730df5b1477c307bf976e94f9c05329c5322c5b431`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04913bca25e195366a3830bada211999e720a1a6093b576ea62209686bea6f4`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452b0da22ef61b1ed15e78d38a817cc3966260f7d78a64c2a28b05fce416995`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed15771250801f0c87551c23c1364b0314f7a8c3951e4b1219c6c6430507f59`  
		Last Modified: Mon, 01 Dec 2025 20:06:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335c680e8b100a4e9a710c60ddfc0a6ecff1d4e0f2c08de8978c7915d101a310`  
		Last Modified: Mon, 01 Dec 2025 20:06:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30f8b00e0976ff412c0be0b1ae015a38b24a46bc78d3c6f5c69d6388c5649ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598ab8f111b05daa9c651148ecff824b69b4dbe320927dea8bb41ff396437d9b`

```dockerfile
```

-	Layers:
	-	`sha256:0b0983d95cd00fb76ad8247da181d9d5248f80fc69f73ac0c338ac4deeb2d7fa`  
		Last Modified: Mon, 01 Dec 2025 22:49:58 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a593463cbc3623f694ac1f939edee81480e2ece7ff61c23c08119cdffe649c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217281108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4744404b490acc86290091007a95de84ea7f68bf06f8af0baead268c76356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 20:04:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:47 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:47 GMT
ARG VERSION=25.10.3.100
# Mon, 01 Dec 2025 20:04:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:17 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:17 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.3.100 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:18 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d5618a252cc58692a14ff5beae75f2ff42fac7881b91e4de2f5832850c63e5`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 7.6 MB (7576744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca96168027ac3934ed3848a116652491fa0a1c01004f63a9f1b197b67d4730`  
		Last Modified: Mon, 01 Dec 2025 22:50:30 GMT  
		Size: 181.5 MB (181450461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c95d11ea9b11716c710608e661d8298430a7dacb4178bea098dae5a380f07`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9412d6c48064ce045f545be8ba9486305e9565e6f4836be74f7cf8b5053a202`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937ccd4d46c777769d56d07e11b6dc9858d51c33abea9edeb688fd237e2b557`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa56fab2fea4770d737655f82ddb959347a3052192fe1055a49720cfbcdd2f45`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d847816d33f078a5734f381fbd1ce4023e65189207167d11e70fa15fa2a70`  
		Last Modified: Mon, 01 Dec 2025 20:06:02 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:17bd58911ae219d07beb472e5264efbaa7f280a47fd2c3594b990da1eba0d30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1d17051f76d7ab03fee2d81d1eb2cd2e8d2ee34ba890faee48e51593900f21`

```dockerfile
```

-	Layers:
	-	`sha256:91a08a09ef402d13bbdf7bcb2f87f925fef70df83a0cda20a6df42a16c3dff0b`  
		Last Modified: Mon, 01 Dec 2025 22:50:01 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.10.4-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.10.4.104`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.10.4.104-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:b757765452c6ad8ddb264b65214ad14d10aea66b9cba4104d76e1dc6bbf53619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:a6ea7a5e036f386b008b3606e12279461c9af474f2486b758633a46fa3ab3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a90e79657a8cac221fab619707cdb26d9f1df3f3c246b6a9f7aae941e010b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:55 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:55 GMT
ARG VERSION=25.11.5.8
# Sun, 28 Dec 2025 05:49:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:20 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:21 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eed9c705ae3b660656601b612f661d47917c4d19559425cafed13d2f32ce64`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 7.6 MB (7598492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6958dc9def1bf5fa7670108f8f5cb13e9599ca5f5c9d462080b74dfe099b5bf`  
		Last Modified: Sun, 28 Dec 2025 07:49:48 GMT  
		Size: 195.9 MB (195881136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510552e5784c1d255db525f5e49801f6a967402f597b1189d05d1c1768002fb6`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf96a9599e819d2cfdf7b71c01e72df0e2fc4527d1c5041a5c080314b3cb880`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2002da93d4a8a477e37df8e8f0de11f6bc107f67a67371b7f0c8762a962e870a`  
		Last Modified: Sun, 28 Dec 2025 05:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ffc9d0a06d1d2b60386d619966ef4d325c05b98d6a53639c34fc7f161e4ef`  
		Last Modified: Sun, 28 Dec 2025 05:50:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6eb637eb688d958c0d70210a5aef9126b79de2df6b4f18cc0c829cd0de77dc`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1b707a0adfe386d07f901570cf486bb2e1e3a31780d578fd5f09e60661201275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7313b612c4066a887bc6246ddfd8700aa8a779cf6ef88aadfde511fbf1f76275`

```dockerfile
```

-	Layers:
	-	`sha256:0fd639ed2e868da084a1a5ad3228f60e515bdf0c1806d96ca973dfc29747a663`  
		Last Modified: Sun, 28 Dec 2025 07:49:24 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2c6b494ad13a31cea3dc68887bac4b87c155d815267f0eb1c9c364d801d5c939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218818546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea255d5ef3733faff18faffad4e0f4b8289f9c76bac7333f920c79768cead47b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:07 GMT
ARG VERSION=25.11.5.8
# Sun, 28 Dec 2025 05:51:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:33 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:33 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2409e0d48452e44438b8a71ae7e22b90f5a126197e5195d737b43dd8315cae0e`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a982d7b71c9fb95d621857104398a86e3c7c3beeb6ceb005f8a59882d48f28e`  
		Last Modified: Sun, 28 Dec 2025 05:55:17 GMT  
		Size: 183.0 MB (182987844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d780faabf0c72fc46cd3c874cd38c593c03f51617eca4d43d1e440d54fb2b3c`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2e00d29dc6bd0ab3238a534200d523ac3e9917e4dae66ab15d549251f95bf`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ba11f578636d4a0d23231bcc3350deaf0a4c3e275a17de19bff889c9956290`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb121dac097f7252a2ac6d6c00daf869f126606b4926866abc26fc40de201915`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1662b99dd787407566d33ec509f0b7493d21daa3cb709a2aa04c9bd30cb11f0`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:85b8a1bdca6054563445e04d0a50bb3caa2bc7520facf7e11bf2a6c9a02ca328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413bbc6b186d9406767c45026f92aefee26ef07f49624a36c371fa5be4d7258d`

```dockerfile
```

-	Layers:
	-	`sha256:909cd2ab193c6f9e6f5cb90c7e829bdef15cb6a659c5b8f6e5b2dfb67255b539`  
		Last Modified: Sun, 28 Dec 2025 07:49:26 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:b757765452c6ad8ddb264b65214ad14d10aea66b9cba4104d76e1dc6bbf53619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:a6ea7a5e036f386b008b3606e12279461c9af474f2486b758633a46fa3ab3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a90e79657a8cac221fab619707cdb26d9f1df3f3c246b6a9f7aae941e010b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:55 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:55 GMT
ARG VERSION=25.11.5.8
# Sun, 28 Dec 2025 05:49:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:20 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:21 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eed9c705ae3b660656601b612f661d47917c4d19559425cafed13d2f32ce64`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 7.6 MB (7598492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6958dc9def1bf5fa7670108f8f5cb13e9599ca5f5c9d462080b74dfe099b5bf`  
		Last Modified: Sun, 28 Dec 2025 07:49:48 GMT  
		Size: 195.9 MB (195881136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510552e5784c1d255db525f5e49801f6a967402f597b1189d05d1c1768002fb6`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf96a9599e819d2cfdf7b71c01e72df0e2fc4527d1c5041a5c080314b3cb880`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2002da93d4a8a477e37df8e8f0de11f6bc107f67a67371b7f0c8762a962e870a`  
		Last Modified: Sun, 28 Dec 2025 05:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ffc9d0a06d1d2b60386d619966ef4d325c05b98d6a53639c34fc7f161e4ef`  
		Last Modified: Sun, 28 Dec 2025 05:50:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6eb637eb688d958c0d70210a5aef9126b79de2df6b4f18cc0c829cd0de77dc`  
		Last Modified: Sun, 28 Dec 2025 05:50:53 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1b707a0adfe386d07f901570cf486bb2e1e3a31780d578fd5f09e60661201275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7313b612c4066a887bc6246ddfd8700aa8a779cf6ef88aadfde511fbf1f76275`

```dockerfile
```

-	Layers:
	-	`sha256:0fd639ed2e868da084a1a5ad3228f60e515bdf0c1806d96ca973dfc29747a663`  
		Last Modified: Sun, 28 Dec 2025 07:49:24 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2c6b494ad13a31cea3dc68887bac4b87c155d815267f0eb1c9c364d801d5c939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218818546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea255d5ef3733faff18faffad4e0f4b8289f9c76bac7333f920c79768cead47b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:07 GMT
ARG VERSION=25.11.5.8
# Sun, 28 Dec 2025 05:51:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:33 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.5.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:33 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2409e0d48452e44438b8a71ae7e22b90f5a126197e5195d737b43dd8315cae0e`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a982d7b71c9fb95d621857104398a86e3c7c3beeb6ceb005f8a59882d48f28e`  
		Last Modified: Sun, 28 Dec 2025 05:55:17 GMT  
		Size: 183.0 MB (182987844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d780faabf0c72fc46cd3c874cd38c593c03f51617eca4d43d1e440d54fb2b3c`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2e00d29dc6bd0ab3238a534200d523ac3e9917e4dae66ab15d549251f95bf`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ba11f578636d4a0d23231bcc3350deaf0a4c3e275a17de19bff889c9956290`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb121dac097f7252a2ac6d6c00daf869f126606b4926866abc26fc40de201915`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1662b99dd787407566d33ec509f0b7493d21daa3cb709a2aa04c9bd30cb11f0`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:85b8a1bdca6054563445e04d0a50bb3caa2bc7520facf7e11bf2a6c9a02ca328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413bbc6b186d9406767c45026f92aefee26ef07f49624a36c371fa5be4d7258d`

```dockerfile
```

-	Layers:
	-	`sha256:909cd2ab193c6f9e6f5cb90c7e829bdef15cb6a659c5b8f6e5b2dfb67255b539`  
		Last Modified: Sun, 28 Dec 2025 07:49:26 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.11.6-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.11.6.11`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.11.6.11-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:c4294111c4a19b15915aaa0f48f89b180386010f0c4dc36167e6df0e208a17fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:3afe75a125f265f74f08083c146438afbe4d80c77cdadbcd47bd5f0dd41c3f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246249652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bcdf7c36a7d427b596dc6f51bf4cec4f03a0257d28d72d2e766ed0749c7ae8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:14 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:49:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:49:40 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:49:40 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:49:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9fd2332cce7e900ed8af1a3639928d452adc512bcb9372061322d1b974517`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadc245bf45d7cc24f5e9c4de1076a71a56cb03374d0b3877f276f2735b17e9`  
		Last Modified: Sun, 28 Dec 2025 07:50:06 GMT  
		Size: 208.2 MB (208244336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264c0fec6269dd512871d70dbd8bda265caa48f7b9f424d9022429f712a7e74`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2be3a440d1d82b64f4772f6355977e909102b14a8ec3feccf4d35da713d143`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c9ae75a5260e4f5ccef9c53addbd48f3993303465273b94395e6fd691a76c`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230e290cfaf7a7f8ff3574828a94d4aa7a84afdabe45d7ff9a8244b316dbe1b`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80525464992be8df1e67a44d8f3bf9f81cebc9fe0597e31c4e37f2f20c2be4d4`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc6044a2b7e396e2ea377d2df44df780a77218041ab003123cc29f7ca0c0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496064297d47e4185d1b5e972d92e84e2720dd77ffd0831a186f4a14a8254fa`

```dockerfile
```

-	Layers:
	-	`sha256:039cfdf5e88ca9cf2c71fdee35fd59604f38cc16b9e88bdf4ef6d84b59dd2485`  
		Last Modified: Sun, 28 Dec 2025 07:49:41 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654733f787256d1730c7e0ca3fcf4494d1ffa1e58ad1155b8ce4801314c13301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228184632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6713b0c091bf6755f4dd9f64437d36deb8a1d0f74001e41b6441414906e5e5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:04 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:51:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:32 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:32 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571441ce734fb443ab487e1c54715675ff2aad732c04a05a770044f8360c928`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5519a7edc0f888b52edb63e3a5db88119261d1c44643f28c7e5793b01e69d34`  
		Last Modified: Sun, 28 Dec 2025 05:58:24 GMT  
		Size: 192.4 MB (192353884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6b7489f49a835d8a84d85fa4881dcf4cc3d0959595caff72f017d8c2eb5fcc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8eb50860e45c27b8af50e1025f7621e9930f293dfad416d82ae11c24e22cc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21ccae9abb9521b2ecf989244f34c03115c0029c321db426bc2253a311b7bb`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9cc36b689c41a4653eca45bff2553349d7491f4a82bb44d1499ec748f5266`  
		Last Modified: Sun, 28 Dec 2025 05:52:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a2ab66ad51068e6e3da2ca920be9f6078f8ab9a25953ee3a500d7d80de717`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8976a39dce64df45042c33f7c990c3f6ef468c14bc3f8640bd778e5bdcb06f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d6fb4c9fdc21033143dbf7cc55c133c908691e850e483351a56ee4abc9c3a`

```dockerfile
```

-	Layers:
	-	`sha256:29de2d8bed1313656227289e93d97b4a993d15f34153768fb4a13991a184c58b`  
		Last Modified: Sun, 28 Dec 2025 07:49:46 GMT  
		Size: 26.3 KB (26274 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:c4294111c4a19b15915aaa0f48f89b180386010f0c4dc36167e6df0e208a17fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3afe75a125f265f74f08083c146438afbe4d80c77cdadbcd47bd5f0dd41c3f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246249652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bcdf7c36a7d427b596dc6f51bf4cec4f03a0257d28d72d2e766ed0749c7ae8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:14 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:49:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:49:40 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:49:40 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:49:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9fd2332cce7e900ed8af1a3639928d452adc512bcb9372061322d1b974517`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadc245bf45d7cc24f5e9c4de1076a71a56cb03374d0b3877f276f2735b17e9`  
		Last Modified: Sun, 28 Dec 2025 07:50:06 GMT  
		Size: 208.2 MB (208244336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264c0fec6269dd512871d70dbd8bda265caa48f7b9f424d9022429f712a7e74`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2be3a440d1d82b64f4772f6355977e909102b14a8ec3feccf4d35da713d143`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c9ae75a5260e4f5ccef9c53addbd48f3993303465273b94395e6fd691a76c`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230e290cfaf7a7f8ff3574828a94d4aa7a84afdabe45d7ff9a8244b316dbe1b`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80525464992be8df1e67a44d8f3bf9f81cebc9fe0597e31c4e37f2f20c2be4d4`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc6044a2b7e396e2ea377d2df44df780a77218041ab003123cc29f7ca0c0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496064297d47e4185d1b5e972d92e84e2720dd77ffd0831a186f4a14a8254fa`

```dockerfile
```

-	Layers:
	-	`sha256:039cfdf5e88ca9cf2c71fdee35fd59604f38cc16b9e88bdf4ef6d84b59dd2485`  
		Last Modified: Sun, 28 Dec 2025 07:49:41 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654733f787256d1730c7e0ca3fcf4494d1ffa1e58ad1155b8ce4801314c13301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228184632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6713b0c091bf6755f4dd9f64437d36deb8a1d0f74001e41b6441414906e5e5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:04 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:51:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:32 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:32 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571441ce734fb443ab487e1c54715675ff2aad732c04a05a770044f8360c928`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5519a7edc0f888b52edb63e3a5db88119261d1c44643f28c7e5793b01e69d34`  
		Last Modified: Sun, 28 Dec 2025 05:58:24 GMT  
		Size: 192.4 MB (192353884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6b7489f49a835d8a84d85fa4881dcf4cc3d0959595caff72f017d8c2eb5fcc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8eb50860e45c27b8af50e1025f7621e9930f293dfad416d82ae11c24e22cc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21ccae9abb9521b2ecf989244f34c03115c0029c321db426bc2253a311b7bb`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9cc36b689c41a4653eca45bff2553349d7491f4a82bb44d1499ec748f5266`  
		Last Modified: Sun, 28 Dec 2025 05:52:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a2ab66ad51068e6e3da2ca920be9f6078f8ab9a25953ee3a500d7d80de717`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8976a39dce64df45042c33f7c990c3f6ef468c14bc3f8640bd778e5bdcb06f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d6fb4c9fdc21033143dbf7cc55c133c908691e850e483351a56ee4abc9c3a`

```dockerfile
```

-	Layers:
	-	`sha256:29de2d8bed1313656227289e93d97b4a993d15f34153768fb4a13991a184c58b`  
		Last Modified: Sun, 28 Dec 2025 07:49:46 GMT  
		Size: 26.3 KB (26274 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.2`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.2-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.2.54`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.2.54-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:f506fb743eb817724c71b5c2cdca0ef898e61cd6edc55b3062a651727466d80f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef6222d6ebf4c764835117b91a3899e0e1d90810187e4a543576be2e3b01e2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206305019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a6cbeb0931fd7cd2bc98675e4a3be421a1fbb0b245a4226a1364502ebfad27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:24 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:24 GMT
ARG VERSION=25.3.11.20
# Sun, 28 Dec 2025 05:50:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:48 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:48 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61b0086f48c51bca8ed43b121a27a6501214cb6b7b1f28972152b83023cf03`  
		Last Modified: Sun, 28 Dec 2025 05:51:17 GMT  
		Size: 7.2 MB (7151671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b7a9673fdf066c9cdab2114accb43390848a52f72683f46571202a8fcdfaac`  
		Last Modified: Sun, 28 Dec 2025 05:57:56 GMT  
		Size: 168.7 MB (168746305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41947d2d017c51ab5626caefb8e09bd74e5a769ee2d33d7860c57d0e79017871`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e77bfe643c82572746e92a4bc7249c6f52f01b37c49e05465b969a5bf8b885`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefd39738fd2ee3d7744560a772e3415020b9b5bcf9152b24d739da1bc22942e`  
		Last Modified: Sun, 28 Dec 2025 05:51:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff305d75d1006a199ec1538d85b00896ab1fc1e93115ee495e9e126adc2b5`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6061e93d1de3809805f23287b889bd5241c4aaf320602546f7521531fb4b11`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9689a7625a99a131db2717153d04b9168a1cccc14cbab7ff814a3aed52d5ee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0010c4f64d314a3ac4dc4b4dc44995d3a0eb2c262e0a3003470d8667b2d17ae2`

```dockerfile
```

-	Layers:
	-	`sha256:2d5c368b32e44957d6e2aa95dea3d925f77fc6a6446200950f752a57ca70570f`  
		Last Modified: Sun, 28 Dec 2025 07:49:59 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:100309e4b56b13427ee4ca676fc355638ff6faacd28c3ccbfb0607e3dc788d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193786125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e183e96eda96d37dd2d0d9bdda2f1bab87b17f4d66ca133dd75b05890a42f1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:52:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:52:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:52:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:52:16 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:52:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:52:16 GMT
ARG VERSION=25.3.11.20
# Sun, 28 Dec 2025 05:52:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:44 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:44 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb16c12e7082f024eda58e1cb4a9b01f52b22379f798543a237e04021a3a494`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 7.1 MB (7127225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd03e0d21448d17694b64077dfe7bf9195ff20c05e200a6de8e1ff98f576e0`  
		Last Modified: Sun, 28 Dec 2025 05:59:03 GMT  
		Size: 158.4 MB (158404780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c63c9d0e52349bb16befea12b74d01b8f974d36f8ddf01d683ad65907aadf9`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c82d454aa3997a30a24413f232779fc14c175b733a180c352cc80b36e7d2a3`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cac46429b2ee9feb3daee609e61987e04b8c572f239187433ed7eafd2bcbf8`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac32c5cd7dc9aa557dac5c334eef8b16579fc594c8e0ca483318b886764dcb7`  
		Last Modified: Sun, 28 Dec 2025 05:53:13 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c578d3d15d154726cc39048b9bbc64be0a6579be30f66bea8f9da0cab2cee0`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d893a8f849e1c09066c159424c22aab5d60f09d14252d7319b0a9c39cd572a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d7cd07c1e28f31232037f810387fa1b35462bf3d201871d0bc22311d4188fd`

```dockerfile
```

-	Layers:
	-	`sha256:a291132ea9a5c0b2e865a9adabe71bfc22320969d27e18e3ce8aee324e17cfac`  
		Last Modified: Sun, 28 Dec 2025 07:50:02 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:f506fb743eb817724c71b5c2cdca0ef898e61cd6edc55b3062a651727466d80f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef6222d6ebf4c764835117b91a3899e0e1d90810187e4a543576be2e3b01e2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206305019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a6cbeb0931fd7cd2bc98675e4a3be421a1fbb0b245a4226a1364502ebfad27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:24 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:24 GMT
ARG VERSION=25.3.11.20
# Sun, 28 Dec 2025 05:50:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:48 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:48 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61b0086f48c51bca8ed43b121a27a6501214cb6b7b1f28972152b83023cf03`  
		Last Modified: Sun, 28 Dec 2025 05:51:17 GMT  
		Size: 7.2 MB (7151671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b7a9673fdf066c9cdab2114accb43390848a52f72683f46571202a8fcdfaac`  
		Last Modified: Sun, 28 Dec 2025 05:57:56 GMT  
		Size: 168.7 MB (168746305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41947d2d017c51ab5626caefb8e09bd74e5a769ee2d33d7860c57d0e79017871`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e77bfe643c82572746e92a4bc7249c6f52f01b37c49e05465b969a5bf8b885`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefd39738fd2ee3d7744560a772e3415020b9b5bcf9152b24d739da1bc22942e`  
		Last Modified: Sun, 28 Dec 2025 05:51:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ff305d75d1006a199ec1538d85b00896ab1fc1e93115ee495e9e126adc2b5`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6061e93d1de3809805f23287b889bd5241c4aaf320602546f7521531fb4b11`  
		Last Modified: Sun, 28 Dec 2025 05:51:16 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9689a7625a99a131db2717153d04b9168a1cccc14cbab7ff814a3aed52d5ee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0010c4f64d314a3ac4dc4b4dc44995d3a0eb2c262e0a3003470d8667b2d17ae2`

```dockerfile
```

-	Layers:
	-	`sha256:2d5c368b32e44957d6e2aa95dea3d925f77fc6a6446200950f752a57ca70570f`  
		Last Modified: Sun, 28 Dec 2025 07:49:59 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:100309e4b56b13427ee4ca676fc355638ff6faacd28c3ccbfb0607e3dc788d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193786125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e183e96eda96d37dd2d0d9bdda2f1bab87b17f4d66ca133dd75b05890a42f1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:52:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:52:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:52:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:52:16 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:52:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:52:16 GMT
ARG VERSION=25.3.11.20
# Sun, 28 Dec 2025 05:52:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:44 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.11.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:44 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb16c12e7082f024eda58e1cb4a9b01f52b22379f798543a237e04021a3a494`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 7.1 MB (7127225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadd03e0d21448d17694b64077dfe7bf9195ff20c05e200a6de8e1ff98f576e0`  
		Last Modified: Sun, 28 Dec 2025 05:59:03 GMT  
		Size: 158.4 MB (158404780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c63c9d0e52349bb16befea12b74d01b8f974d36f8ddf01d683ad65907aadf9`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c82d454aa3997a30a24413f232779fc14c175b733a180c352cc80b36e7d2a3`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cac46429b2ee9feb3daee609e61987e04b8c572f239187433ed7eafd2bcbf8`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac32c5cd7dc9aa557dac5c334eef8b16579fc594c8e0ca483318b886764dcb7`  
		Last Modified: Sun, 28 Dec 2025 05:53:13 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c578d3d15d154726cc39048b9bbc64be0a6579be30f66bea8f9da0cab2cee0`  
		Last Modified: Sun, 28 Dec 2025 05:53:11 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d893a8f849e1c09066c159424c22aab5d60f09d14252d7319b0a9c39cd572a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d7cd07c1e28f31232037f810387fa1b35462bf3d201871d0bc22311d4188fd`

```dockerfile
```

-	Layers:
	-	`sha256:a291132ea9a5c0b2e865a9adabe71bfc22320969d27e18e3ce8aee324e17cfac`  
		Last Modified: Sun, 28 Dec 2025 07:50:02 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.12-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.12.8`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.12.8-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:1b39248023fa9a1e412bb6f8ed4cccfaf945ebe2d974bd1e06702b5c9da07d1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:57717a53e1bd7b94576d28020e60b039124f5f465a478d5245bdd44acc1a5e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228921188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06c0426fd0126804c9fa62215fadbe795ce638213a72e9a4df8e31e107225`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:07 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:50:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:34 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:34 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb4182df99a4ce23c85b1c8483ee235b6addfe4e0d45b043e7b64aff16ba47`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ea53e42b6649f3cf10cbdddf9e88fcd6313442730a58cb114f60840a6cc53`  
		Last Modified: Sun, 28 Dec 2025 05:59:42 GMT  
		Size: 190.9 MB (190915903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd83eb0674d0b031460827ae7e1efaacc7dfd15e702eb8b4c0674a6d34070d0`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9873fffd080a0374b56b2244bc8503ea466936c1ce5cbd6044f93f6a26936cc`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e5313f7fc8af2d2f1ff73ada4a17b68b6d5a9caf9f1fb6d3bcac15313c146`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6b396e2475c1116017e9551dedb2d9801ef76cc4f4985161a76b3f15fb81f`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf6ff6e01dacf79154a589dcd07d243adfd45445629008d96a1f171d1f87297`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4af228da1ac4717c50b97c44d40f3d79d40c49f7f9077d896b7874e5974638ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d79a471de821dde344bff071d94c9152d88961fd924e0e3171a6a2424ce6c8`

```dockerfile
```

-	Layers:
	-	`sha256:268522c16940da626d3ef942c1ded212b21da22bdd293a1fe831c8a8ff328be5`  
		Last Modified: Sun, 28 Dec 2025 07:50:18 GMT  
		Size: 26.0 KB (26044 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:076faba96df7333b8a000b7b73799fd426f880309a51f51e440c15fb6e8f2153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213826163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc6ba9c0467cc13f3bb729910286399d2ae2f2a159808740239f0a945412edf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:37 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:51:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:09 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:09 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb333022a21a456c491fb4e2206ca9ef18c1c350136616241cf2c033fce2704`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a017d1336770a1213233733473a63e1e78276c0d31df533de071e7da1304fe0d`  
		Last Modified: Sun, 28 Dec 2025 06:15:34 GMT  
		Size: 178.0 MB (177995529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e7d332e1d19e76a19ce773dde85a282cf42c431e8cabcbada3979081208ec3`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947061c155c1940b4b6e3dc60715fc5d85675b66443fca2b427ac64fffa6b6b8`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd222c3d00ae5d2eec00efd54c44f0779a71f209e824e13f7efa96e7b8ce1b`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b8208998015a689556eb8c2088281d2e2c333d5f448c3032432e0e8893487`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77591cb578d1cae215b757a36d22caa1f0f79f197db23b2fecfc5349b673017e`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fbd6f5a900b7f9e80bf541e5bc47e8d2554372b715a08f171d4a3d98cf51f155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537d1c35986b7d00cf391beb9d33828342be00aa660359d6603e9c06481e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:c01e652661d1fb136ec0d6b72ab88c91739897335b196c6bf1eb73da8a184c7f`  
		Last Modified: Sun, 28 Dec 2025 07:50:21 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:1b39248023fa9a1e412bb6f8ed4cccfaf945ebe2d974bd1e06702b5c9da07d1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:57717a53e1bd7b94576d28020e60b039124f5f465a478d5245bdd44acc1a5e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228921188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06c0426fd0126804c9fa62215fadbe795ce638213a72e9a4df8e31e107225`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:07 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:50:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:34 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:34 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb4182df99a4ce23c85b1c8483ee235b6addfe4e0d45b043e7b64aff16ba47`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ea53e42b6649f3cf10cbdddf9e88fcd6313442730a58cb114f60840a6cc53`  
		Last Modified: Sun, 28 Dec 2025 05:59:42 GMT  
		Size: 190.9 MB (190915903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd83eb0674d0b031460827ae7e1efaacc7dfd15e702eb8b4c0674a6d34070d0`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9873fffd080a0374b56b2244bc8503ea466936c1ce5cbd6044f93f6a26936cc`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e5313f7fc8af2d2f1ff73ada4a17b68b6d5a9caf9f1fb6d3bcac15313c146`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6b396e2475c1116017e9551dedb2d9801ef76cc4f4985161a76b3f15fb81f`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf6ff6e01dacf79154a589dcd07d243adfd45445629008d96a1f171d1f87297`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4af228da1ac4717c50b97c44d40f3d79d40c49f7f9077d896b7874e5974638ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d79a471de821dde344bff071d94c9152d88961fd924e0e3171a6a2424ce6c8`

```dockerfile
```

-	Layers:
	-	`sha256:268522c16940da626d3ef942c1ded212b21da22bdd293a1fe831c8a8ff328be5`  
		Last Modified: Sun, 28 Dec 2025 07:50:18 GMT  
		Size: 26.0 KB (26044 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:076faba96df7333b8a000b7b73799fd426f880309a51f51e440c15fb6e8f2153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213826163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc6ba9c0467cc13f3bb729910286399d2ae2f2a159808740239f0a945412edf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:37 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:51:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:09 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:09 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb333022a21a456c491fb4e2206ca9ef18c1c350136616241cf2c033fce2704`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a017d1336770a1213233733473a63e1e78276c0d31df533de071e7da1304fe0d`  
		Last Modified: Sun, 28 Dec 2025 06:15:34 GMT  
		Size: 178.0 MB (177995529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e7d332e1d19e76a19ce773dde85a282cf42c431e8cabcbada3979081208ec3`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947061c155c1940b4b6e3dc60715fc5d85675b66443fca2b427ac64fffa6b6b8`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd222c3d00ae5d2eec00efd54c44f0779a71f209e824e13f7efa96e7b8ce1b`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b8208998015a689556eb8c2088281d2e2c333d5f448c3032432e0e8893487`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77591cb578d1cae215b757a36d22caa1f0f79f197db23b2fecfc5349b673017e`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fbd6f5a900b7f9e80bf541e5bc47e8d2554372b715a08f171d4a3d98cf51f155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537d1c35986b7d00cf391beb9d33828342be00aa660359d6603e9c06481e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:c01e652661d1fb136ec0d6b72ab88c91739897335b196c6bf1eb73da8a184c7f`  
		Last Modified: Sun, 28 Dec 2025 07:50:21 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.8.14-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.8.14.17`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.8.14.17-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:c4294111c4a19b15915aaa0f48f89b180386010f0c4dc36167e6df0e208a17fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3afe75a125f265f74f08083c146438afbe4d80c77cdadbcd47bd5f0dd41c3f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246249652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bcdf7c36a7d427b596dc6f51bf4cec4f03a0257d28d72d2e766ed0749c7ae8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:14 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:49:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:49:40 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:49:40 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:49:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9fd2332cce7e900ed8af1a3639928d452adc512bcb9372061322d1b974517`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadc245bf45d7cc24f5e9c4de1076a71a56cb03374d0b3877f276f2735b17e9`  
		Last Modified: Sun, 28 Dec 2025 07:50:06 GMT  
		Size: 208.2 MB (208244336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264c0fec6269dd512871d70dbd8bda265caa48f7b9f424d9022429f712a7e74`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2be3a440d1d82b64f4772f6355977e909102b14a8ec3feccf4d35da713d143`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c9ae75a5260e4f5ccef9c53addbd48f3993303465273b94395e6fd691a76c`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230e290cfaf7a7f8ff3574828a94d4aa7a84afdabe45d7ff9a8244b316dbe1b`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80525464992be8df1e67a44d8f3bf9f81cebc9fe0597e31c4e37f2f20c2be4d4`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc6044a2b7e396e2ea377d2df44df780a77218041ab003123cc29f7ca0c0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496064297d47e4185d1b5e972d92e84e2720dd77ffd0831a186f4a14a8254fa`

```dockerfile
```

-	Layers:
	-	`sha256:039cfdf5e88ca9cf2c71fdee35fd59604f38cc16b9e88bdf4ef6d84b59dd2485`  
		Last Modified: Sun, 28 Dec 2025 07:49:41 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654733f787256d1730c7e0ca3fcf4494d1ffa1e58ad1155b8ce4801314c13301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228184632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6713b0c091bf6755f4dd9f64437d36deb8a1d0f74001e41b6441414906e5e5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:04 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:51:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:32 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:32 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571441ce734fb443ab487e1c54715675ff2aad732c04a05a770044f8360c928`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5519a7edc0f888b52edb63e3a5db88119261d1c44643f28c7e5793b01e69d34`  
		Last Modified: Sun, 28 Dec 2025 05:58:24 GMT  
		Size: 192.4 MB (192353884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6b7489f49a835d8a84d85fa4881dcf4cc3d0959595caff72f017d8c2eb5fcc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8eb50860e45c27b8af50e1025f7621e9930f293dfad416d82ae11c24e22cc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21ccae9abb9521b2ecf989244f34c03115c0029c321db426bc2253a311b7bb`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9cc36b689c41a4653eca45bff2553349d7491f4a82bb44d1499ec748f5266`  
		Last Modified: Sun, 28 Dec 2025 05:52:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a2ab66ad51068e6e3da2ca920be9f6078f8ab9a25953ee3a500d7d80de717`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8976a39dce64df45042c33f7c990c3f6ef468c14bc3f8640bd778e5bdcb06f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d6fb4c9fdc21033143dbf7cc55c133c908691e850e483351a56ee4abc9c3a`

```dockerfile
```

-	Layers:
	-	`sha256:29de2d8bed1313656227289e93d97b4a993d15f34153768fb4a13991a184c58b`  
		Last Modified: Sun, 28 Dec 2025 07:49:46 GMT  
		Size: 26.3 KB (26274 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:c4294111c4a19b15915aaa0f48f89b180386010f0c4dc36167e6df0e208a17fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:3afe75a125f265f74f08083c146438afbe4d80c77cdadbcd47bd5f0dd41c3f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246249652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bcdf7c36a7d427b596dc6f51bf4cec4f03a0257d28d72d2e766ed0749c7ae8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:49:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:49:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:49:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:49:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:49:14 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:49:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:49:40 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:49:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:49:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:49:40 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:49:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:49:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9fd2332cce7e900ed8af1a3639928d452adc512bcb9372061322d1b974517`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadc245bf45d7cc24f5e9c4de1076a71a56cb03374d0b3877f276f2735b17e9`  
		Last Modified: Sun, 28 Dec 2025 07:50:06 GMT  
		Size: 208.2 MB (208244336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264c0fec6269dd512871d70dbd8bda265caa48f7b9f424d9022429f712a7e74`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2be3a440d1d82b64f4772f6355977e909102b14a8ec3feccf4d35da713d143`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c9ae75a5260e4f5ccef9c53addbd48f3993303465273b94395e6fd691a76c`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230e290cfaf7a7f8ff3574828a94d4aa7a84afdabe45d7ff9a8244b316dbe1b`  
		Last Modified: Sun, 28 Dec 2025 05:50:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80525464992be8df1e67a44d8f3bf9f81cebc9fe0597e31c4e37f2f20c2be4d4`  
		Last Modified: Sun, 28 Dec 2025 05:50:12 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc6044a2b7e396e2ea377d2df44df780a77218041ab003123cc29f7ca0c0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496064297d47e4185d1b5e972d92e84e2720dd77ffd0831a186f4a14a8254fa`

```dockerfile
```

-	Layers:
	-	`sha256:039cfdf5e88ca9cf2c71fdee35fd59604f38cc16b9e88bdf4ef6d84b59dd2485`  
		Last Modified: Sun, 28 Dec 2025 07:49:41 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654733f787256d1730c7e0ca3fcf4494d1ffa1e58ad1155b8ce4801314c13301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228184632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6713b0c091bf6755f4dd9f64437d36deb8a1d0f74001e41b6441414906e5e5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:04 GMT
ARG VERSION=25.12.1.649
# Sun, 28 Dec 2025 05:51:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:51:32 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:51:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.1.649 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:51:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:51:32 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:51:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:51:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571441ce734fb443ab487e1c54715675ff2aad732c04a05a770044f8360c928`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 7.6 MB (7576824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5519a7edc0f888b52edb63e3a5db88119261d1c44643f28c7e5793b01e69d34`  
		Last Modified: Sun, 28 Dec 2025 05:58:24 GMT  
		Size: 192.4 MB (192353884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6b7489f49a835d8a84d85fa4881dcf4cc3d0959595caff72f017d8c2eb5fcc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8eb50860e45c27b8af50e1025f7621e9930f293dfad416d82ae11c24e22cc`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21ccae9abb9521b2ecf989244f34c03115c0029c321db426bc2253a311b7bb`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9cc36b689c41a4653eca45bff2553349d7491f4a82bb44d1499ec748f5266`  
		Last Modified: Sun, 28 Dec 2025 05:52:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a2ab66ad51068e6e3da2ca920be9f6078f8ab9a25953ee3a500d7d80de717`  
		Last Modified: Sun, 28 Dec 2025 05:52:03 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8976a39dce64df45042c33f7c990c3f6ef468c14bc3f8640bd778e5bdcb06f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555d6fb4c9fdc21033143dbf7cc55c133c908691e850e483351a56ee4abc9c3a`

```dockerfile
```

-	Layers:
	-	`sha256:29de2d8bed1313656227289e93d97b4a993d15f34153768fb4a13991a184c58b`  
		Last Modified: Sun, 28 Dec 2025 07:49:46 GMT  
		Size: 26.3 KB (26274 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:1b39248023fa9a1e412bb6f8ed4cccfaf945ebe2d974bd1e06702b5c9da07d1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:57717a53e1bd7b94576d28020e60b039124f5f465a478d5245bdd44acc1a5e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228921188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06c0426fd0126804c9fa62215fadbe795ce638213a72e9a4df8e31e107225`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:07 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:50:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:34 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:34 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb4182df99a4ce23c85b1c8483ee235b6addfe4e0d45b043e7b64aff16ba47`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ea53e42b6649f3cf10cbdddf9e88fcd6313442730a58cb114f60840a6cc53`  
		Last Modified: Sun, 28 Dec 2025 05:59:42 GMT  
		Size: 190.9 MB (190915903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd83eb0674d0b031460827ae7e1efaacc7dfd15e702eb8b4c0674a6d34070d0`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9873fffd080a0374b56b2244bc8503ea466936c1ce5cbd6044f93f6a26936cc`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e5313f7fc8af2d2f1ff73ada4a17b68b6d5a9caf9f1fb6d3bcac15313c146`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6b396e2475c1116017e9551dedb2d9801ef76cc4f4985161a76b3f15fb81f`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf6ff6e01dacf79154a589dcd07d243adfd45445629008d96a1f171d1f87297`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4af228da1ac4717c50b97c44d40f3d79d40c49f7f9077d896b7874e5974638ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d79a471de821dde344bff071d94c9152d88961fd924e0e3171a6a2424ce6c8`

```dockerfile
```

-	Layers:
	-	`sha256:268522c16940da626d3ef942c1ded212b21da22bdd293a1fe831c8a8ff328be5`  
		Last Modified: Sun, 28 Dec 2025 07:50:18 GMT  
		Size: 26.0 KB (26044 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:076faba96df7333b8a000b7b73799fd426f880309a51f51e440c15fb6e8f2153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213826163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc6ba9c0467cc13f3bb729910286399d2ae2f2a159808740239f0a945412edf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:37 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:51:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:09 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:09 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb333022a21a456c491fb4e2206ca9ef18c1c350136616241cf2c033fce2704`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a017d1336770a1213233733473a63e1e78276c0d31df533de071e7da1304fe0d`  
		Last Modified: Sun, 28 Dec 2025 06:15:34 GMT  
		Size: 178.0 MB (177995529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e7d332e1d19e76a19ce773dde85a282cf42c431e8cabcbada3979081208ec3`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947061c155c1940b4b6e3dc60715fc5d85675b66443fca2b427ac64fffa6b6b8`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd222c3d00ae5d2eec00efd54c44f0779a71f209e824e13f7efa96e7b8ce1b`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b8208998015a689556eb8c2088281d2e2c333d5f448c3032432e0e8893487`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77591cb578d1cae215b757a36d22caa1f0f79f197db23b2fecfc5349b673017e`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fbd6f5a900b7f9e80bf541e5bc47e8d2554372b715a08f171d4a3d98cf51f155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537d1c35986b7d00cf391beb9d33828342be00aa660359d6603e9c06481e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:c01e652661d1fb136ec0d6b72ab88c91739897335b196c6bf1eb73da8a184c7f`  
		Last Modified: Sun, 28 Dec 2025 07:50:21 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:1b39248023fa9a1e412bb6f8ed4cccfaf945ebe2d974bd1e06702b5c9da07d1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:57717a53e1bd7b94576d28020e60b039124f5f465a478d5245bdd44acc1a5e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228921188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed06c0426fd0126804c9fa62215fadbe795ce638213a72e9a4df8e31e107225`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:50:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:50:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:50:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:50:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:50:07 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:50:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:50:34 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:50:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:50:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:50:34 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:50:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb4182df99a4ce23c85b1c8483ee235b6addfe4e0d45b043e7b64aff16ba47`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 7.6 MB (7598465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ea53e42b6649f3cf10cbdddf9e88fcd6313442730a58cb114f60840a6cc53`  
		Last Modified: Sun, 28 Dec 2025 05:59:42 GMT  
		Size: 190.9 MB (190915903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd83eb0674d0b031460827ae7e1efaacc7dfd15e702eb8b4c0674a6d34070d0`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9873fffd080a0374b56b2244bc8503ea466936c1ce5cbd6044f93f6a26936cc`  
		Last Modified: Sun, 28 Dec 2025 05:51:06 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839e5313f7fc8af2d2f1ff73ada4a17b68b6d5a9caf9f1fb6d3bcac15313c146`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6b396e2475c1116017e9551dedb2d9801ef76cc4f4985161a76b3f15fb81f`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf6ff6e01dacf79154a589dcd07d243adfd45445629008d96a1f171d1f87297`  
		Last Modified: Sun, 28 Dec 2025 05:51:05 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4af228da1ac4717c50b97c44d40f3d79d40c49f7f9077d896b7874e5974638ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d79a471de821dde344bff071d94c9152d88961fd924e0e3171a6a2424ce6c8`

```dockerfile
```

-	Layers:
	-	`sha256:268522c16940da626d3ef942c1ded212b21da22bdd293a1fe831c8a8ff328be5`  
		Last Modified: Sun, 28 Dec 2025 07:50:18 GMT  
		Size: 26.0 KB (26044 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:076faba96df7333b8a000b7b73799fd426f880309a51f51e440c15fb6e8f2153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213826163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc6ba9c0467cc13f3bb729910286399d2ae2f2a159808740239f0a945412edf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Sun, 28 Dec 2025 05:51:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 28 Dec 2025 05:51:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 28 Dec 2025 05:51:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPO_CHANNEL=stable
# Sun, 28 Dec 2025 05:51:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 28 Dec 2025 05:51:37 GMT
ARG VERSION=25.8.13.73
# Sun, 28 Dec 2025 05:51:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
ENV LANG=en_US.UTF-8
# Sun, 28 Dec 2025 05:52:09 GMT
ENV TZ=UTC
# Sun, 28 Dec 2025 05:52:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.13.73 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 28 Dec 2025 05:52:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 28 Dec 2025 05:52:09 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 28 Dec 2025 05:52:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 28 Dec 2025 05:52:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb333022a21a456c491fb4e2206ca9ef18c1c350136616241cf2c033fce2704`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a017d1336770a1213233733473a63e1e78276c0d31df533de071e7da1304fe0d`  
		Last Modified: Sun, 28 Dec 2025 06:15:34 GMT  
		Size: 178.0 MB (177995529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e7d332e1d19e76a19ce773dde85a282cf42c431e8cabcbada3979081208ec3`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947061c155c1940b4b6e3dc60715fc5d85675b66443fca2b427ac64fffa6b6b8`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd222c3d00ae5d2eec00efd54c44f0779a71f209e824e13f7efa96e7b8ce1b`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490b8208998015a689556eb8c2088281d2e2c333d5f448c3032432e0e8893487`  
		Last Modified: Sun, 28 Dec 2025 05:52:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77591cb578d1cae215b757a36d22caa1f0f79f197db23b2fecfc5349b673017e`  
		Last Modified: Sun, 28 Dec 2025 05:52:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fbd6f5a900b7f9e80bf541e5bc47e8d2554372b715a08f171d4a3d98cf51f155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537d1c35986b7d00cf391beb9d33828342be00aa660359d6603e9c06481e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:c01e652661d1fb136ec0d6b72ab88c91739897335b196c6bf1eb73da8a184c7f`  
		Last Modified: Sun, 28 Dec 2025 07:50:21 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
