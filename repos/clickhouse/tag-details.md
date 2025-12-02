<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.10`](#clickhouse2510)
-	[`clickhouse:25.10-jammy`](#clickhouse2510-jammy)
-	[`clickhouse:25.10.3`](#clickhouse25103)
-	[`clickhouse:25.10.3-jammy`](#clickhouse25103-jammy)
-	[`clickhouse:25.10.3.100`](#clickhouse25103100)
-	[`clickhouse:25.10.3.100-jammy`](#clickhouse25103100-jammy)
-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.1`](#clickhouse25111)
-	[`clickhouse:25.11.1-jammy`](#clickhouse25111-jammy)
-	[`clickhouse:25.11.1.558`](#clickhouse25111558)
-	[`clickhouse:25.11.1.558-jammy`](#clickhouse25111558-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.9`](#clickhouse2539)
-	[`clickhouse:25.3.9-jammy`](#clickhouse2539-jammy)
-	[`clickhouse:25.3.9.72`](#clickhouse253972)
-	[`clickhouse:25.3.9.72-jammy`](#clickhouse253972-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.12`](#clickhouse25812)
-	[`clickhouse:25.8.12-jammy`](#clickhouse25812-jammy)
-	[`clickhouse:25.8.12.129`](#clickhouse25812129)
-	[`clickhouse:25.8.12.129-jammy`](#clickhouse25812129-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.6`](#clickhouse2596)
-	[`clickhouse:25.9.6-jammy`](#clickhouse2596-jammy)
-	[`clickhouse:25.9.6.117`](#clickhouse2596117)
-	[`clickhouse:25.9.6.117-jammy`](#clickhouse2596117-jammy)
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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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

## `clickhouse:25.10.3`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.3` - linux; amd64

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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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

### `clickhouse:25.10.3` - unknown; unknown

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

### `clickhouse:25.10.3` - linux; arm64 variant v8

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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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

### `clickhouse:25.10.3` - unknown; unknown

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

## `clickhouse:25.10.3-jammy`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.3-jammy` - linux; amd64

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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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

### `clickhouse:25.10.3-jammy` - unknown; unknown

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

### `clickhouse:25.10.3-jammy` - linux; arm64 variant v8

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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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

### `clickhouse:25.10.3-jammy` - unknown; unknown

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

## `clickhouse:25.10.3.100`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.3.100` - linux; amd64

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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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

### `clickhouse:25.10.3.100` - unknown; unknown

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

### `clickhouse:25.10.3.100` - linux; arm64 variant v8

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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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

### `clickhouse:25.10.3.100` - unknown; unknown

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

## `clickhouse:25.10.3.100-jammy`

```console
$ docker pull clickhouse@sha256:2ce236342e518f8371a1e63f2a10a8f9a602d4105095232e42fcf9c793702046
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.3.100-jammy` - linux; amd64

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
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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

### `clickhouse:25.10.3.100-jammy` - unknown; unknown

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

### `clickhouse:25.10.3.100-jammy` - linux; arm64 variant v8

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
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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

### `clickhouse:25.10.3.100-jammy` - unknown; unknown

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

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.1`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.1-jammy`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.1.558`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.1.558` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1.558` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.1.558` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1.558` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.1.558-jammy`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.1.558-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1.558-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.1.558-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.1.558-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.9`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.9-jammy`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.9.72`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.9.72` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9.72` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.9.72` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9.72` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.9.72-jammy`

```console
$ docker pull clickhouse@sha256:35be7d06e671450a3876010b9ccfc9c8552440ed805a5feff709e8a5767b560a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.9.72-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f9c833373ed59e23556f585bacb6a857d53defd695e23c2b1877c5273680b76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206263975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956be5d3c87645e09db4158acc342fda0f4629bc43295dfefb0022dc58c3424f`
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
# Mon, 01 Dec 2025 20:05:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:54 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:22 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f2be00c102358a0ca5c0e57b4000e08cb044be49be5572393d70edc83fc656`  
		Last Modified: Mon, 01 Dec 2025 20:07:01 GMT  
		Size: 7.2 MB (7151602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcbb4fd269fcaaedb2eb1755118457f952acafb190450b5fd48edd6a3a822e7`  
		Last Modified: Mon, 01 Dec 2025 22:51:22 GMT  
		Size: 168.7 MB (168705324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954765c9b8de350ef05f1c552cdfaa1c8530382967192468f893d279a63c9c`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd98f4085044c082888db08dad42fe27d0f60cbe2f141c06babae2710782fb`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60659c65bb21e617c43ed89a0aa0756458d6b919771ee45cc1cee0ffb2b12b`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea993c801fcec9a001ed0b286d811d046115e9c0e644ca278ed68c70f6f15f`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3e9e6a1631ebd445d77661974a2500bf0a85b3e1359d635495f347e32cc74`  
		Last Modified: Mon, 01 Dec 2025 20:07:00 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9.72-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a3d8ccbef64ff398dc60e7adedadb9d731bb23f3fb4aa41e571a140b757fded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d25ded1ff52883b6b65583dd80246a7f7d3e5e75aa9e4e1647440e8ecd4a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:f492cb2b49b6ab1271cea0e4dd7f301b09efdf6f3babee413dc675f2f71d5e39`  
		Last Modified: Mon, 01 Dec 2025 22:50:33 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.9.72-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:33c3a611f73a3b53c25daf2e0c0e65d68b4f6e022aa04128b955576488781feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193747465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467580a09da3fa4a397566cdb302c926019508b3c83691bf226bcdda42a4c44`
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
# Mon, 01 Dec 2025 20:05:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:28 GMT
ARG VERSION=25.3.9.72
# Mon, 01 Dec 2025 20:05:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:54 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.9.72 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715dfa58e85b220b72fe12af114662e5b52091490b69cb024a6edba6c346e563`  
		Last Modified: Mon, 01 Dec 2025 20:06:30 GMT  
		Size: 7.1 MB (7127251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aca764a92f7431ae99359f0e2d8f8e9620f8121f3f17ffe78da31d5d54b283c`  
		Last Modified: Mon, 01 Dec 2025 22:51:12 GMT  
		Size: 158.4 MB (158366087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c700864964b7b072c9c2e43a34cfb9d27ee6e82ca16f9a3c2e67b4cadeaa4`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201c5f8ef394d857d2fe9a6f88c35ee5711c4ade1e7299ae347c1bdb34b930e`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825dd0a7f71ded52d6d80a98b3b18823629f523682e734986ce2fefb9e0fa0a7`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90b17fc1635ddca1e8daeb588236add9f8647ed005d29c76c6186c3f005ede`  
		Last Modified: Mon, 01 Dec 2025 20:06:29 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.9.72-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dd2fc9939521003ef8db8bbbba1b7ce396b9ca43d13a7fef8e994b583261aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008998bb267bcf977849088792e0b56866ccb2d03e76c73ea8489dccc0af8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:118ffb6937d17deb6f14816b34b39b7c52a0a190e8f34030668a9447f7c58636`  
		Last Modified: Mon, 01 Dec 2025 22:50:36 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.12`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.12-jammy`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.12.129`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.12.129` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12.129` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.12.129` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12.129` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.12.129-jammy`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.12.129-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12.129-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.12.129-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.12.129-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.6`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.6-jammy`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.6.117`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.6.117` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6.117` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.6.117` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6.117` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.6.117-jammy`

```console
$ docker pull clickhouse@sha256:1516eb1f62347f7c3166c85b6afc5d7065164c9cbb7d2cfb035a69ca293f3672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.6.117-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:95eb8abb9722d02f5053cd4318ce49920d2ee7b8666f6f57852413f51f440986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229628380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1812900e15d066de6f8797ae8d0b28dad866080e0742f1b90695b726898f5109`
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
# Mon, 01 Dec 2025 20:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:55 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:33 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:33 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa75a820b5a46e2201930327d38491e7e250b1a79d9b6cb31197a6a05fef47c`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 7.6 MB (7598556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa854ebf3ca89266e185671584c39839f6f209ee5ff2c52a55fc0afaa0a2a28e`  
		Last Modified: Mon, 01 Dec 2025 21:26:18 GMT  
		Size: 191.6 MB (191623000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cef082086ec9f9133d89f74139914fce4b9da042ac14e648659036c7f18c84a`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43802bc2afa35b4e26dcff2f0e16dbc5b22f1bf704c6ed79605cf63456d33817`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e56e25e866ba03afa410fb9c8da6cd1e61baa6cc0f7aa66d79d555204b9ce9`  
		Last Modified: Mon, 01 Dec 2025 20:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f2b034af332d7df0511edad4685c51dd7df1dd05b23db04b3c8721ad38a7f5`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b7ea7e3c979f3fc913d839030fa85e1b7d58052f1bff5f7976f5bbe0afcf0`  
		Last Modified: Mon, 01 Dec 2025 20:07:09 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6.117-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bf9f5ec8d1f7054eae747a9de8dd023fe5cdfdd4188513f1655244d76524f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b46f2263346657f51b29adc859bec4ca9591cfbbb6af3dce7b2e488e8405ece`

```dockerfile
```

-	Layers:
	-	`sha256:0b9a59ff45d3a4e18853081c1f4229e4ae6334e9fcc6963f2050e2ad142908d3`  
		Last Modified: Mon, 01 Dec 2025 22:51:10 GMT  
		Size: 25.4 KB (25429 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.6.117-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:54bde4a4864556f48f9a1730d88a4426acef2da6bf70f0489e57d799f1ace807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214933907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b118a6a4b36a2f6fb71876b241e3cafa15840e951bd818f324f4bad52f4ab2d`
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
# Mon, 01 Dec 2025 20:05:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:25 GMT
ARG VERSION=25.9.6.117
# Mon, 01 Dec 2025 20:05:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:56 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.6.117 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:56 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ef66b085a0df6676db46cb18085b4b1ef09f22cca9cda23fd7c3ca503753`  
		Last Modified: Mon, 01 Dec 2025 20:06:33 GMT  
		Size: 7.6 MB (7576830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d68e52d998a1d702e035e6b593a3b6669b623f23d9c9bb0cffd24c53fa6cc8`  
		Last Modified: Mon, 01 Dec 2025 22:51:39 GMT  
		Size: 179.1 MB (179103176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac1357d4b74bd0a0b017503c11d1d4ebbd2c0d96fb7334724a2c582bc776805`  
		Last Modified: Mon, 01 Dec 2025 20:06:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f081df5d6d2640207eeae0e4e312cf880a90dbc0708c08c3ce9e878bade57a`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce2e78ad737d20463cd8f33f6f7bd2fc9fabeb8c94bafb0b357213faec66ae`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdef2a5841b4624e257de5b1959ec1813a385b45920141e4d4c75966bb8843d`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb6c5907269f9bea229de9e40e5c0bd732beadd71435cfd9f9f5351a475814`  
		Last Modified: Mon, 01 Dec 2025 20:06:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.6.117-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bc7e9074387779eb988a5824bf8555b7c3d4246a1b2ef6f777589173c2ee8ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f386e2711a1c8dc9cce8bdf71496a644b761f01b90deaa5ddab4755be3c8f1`

```dockerfile
```

-	Layers:
	-	`sha256:a53558d8ce1930ff58608fb4010fb71e93d2c8de0b3a9ba5bd39b239a01bcec6`  
		Last Modified: Mon, 01 Dec 2025 22:51:13 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:8002ff593f9adf8b067bf7d6c4995125169ef04d1863882d8ea5cf1b39cce83b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:40569773c8b15150244551b1c69518c9c32611aa6db23ea3857e27623e4898bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233939548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2074e699f54de95b34ef897b1ca710e36a7221b52165b5c75273694f2e110`
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
# Mon, 01 Dec 2025 20:04:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:33 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:04 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:04 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43534f80405ae92163357878154293f9640d76f6f0b264fc419e6b4334ce1a63`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 7.6 MB (7598495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c593278e324ebc2b2bb505a132f98affdf7433e924c90af51c32aa1efcf0f10b`  
		Last Modified: Mon, 01 Dec 2025 21:25:46 GMT  
		Size: 195.9 MB (195934207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f861449fd3de59400175cd229c4ae562453a0ba7a6f9da68d4a1bf7a0c20eb60`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289686a941a9219b75a0a6baf290beae2f352d4ad0f500ef7e4608b9d1e9715`  
		Last Modified: Mon, 01 Dec 2025 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8019f7f55ac966bd462e4d53b5d4c8ca573d85f176ce8a0553757f1124d78`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee0c0c1ea5ba1d40e92f9494db3bde5330cdb88d9ae06b1bc6e5c88eeba4a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5846c48afe41680fc101518e883c0a7df329007a43f55cf134118c15e2b41`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:52f9cc20d96fb6d02c2744fe265dfb156085b6aab4c66b78e9f40cf0b0c8e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131468fdc5e671839fdec88ddc1cddb9222d95403f97f53038a46c851f1bcf78`

```dockerfile
```

-	Layers:
	-	`sha256:671ecf2d073883e5cb5ff7e764786919dda8cad6f423336ffec7aeb6afd3f49e`  
		Last Modified: Mon, 01 Dec 2025 22:50:15 GMT  
		Size: 26.1 KB (26062 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db2206954d67be5effb6ad61b31d0d5ca57e77bb0e24c7575992f779db313c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218703754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc126ccb0257542e27c623aeca7ee2f860545647941199293d5f0504040fa5b`
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
# Mon, 01 Dec 2025 20:04:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:19 GMT
ARG VERSION=25.11.1.558
# Mon, 01 Dec 2025 20:04:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:04:48 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:04:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.1.558 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:04:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:04:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:04:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:04:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea147e0abd5d0819e52f64b261590f6a82c08123b497cb8ce0922a8f255aaf`  
		Last Modified: Mon, 01 Dec 2025 20:06:03 GMT  
		Size: 7.6 MB (7576743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf137ea557d68e208c006ef86f964cee2aae383c30df2c02c253fc33cdab2a`  
		Last Modified: Mon, 01 Dec 2025 22:50:48 GMT  
		Size: 182.9 MB (182873087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34d49cb54dd0ee221b8ce5182b3423a6100c0ea8095cd19ee8b3fe20a49f2c`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f6404324930a8a315c50c0e93265f980993f646f8dea457837b1512d3bd47`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4e8ee1e475dcb8c8baf1277d963b2426cedb2f76f015a909e0c26edf38ec6`  
		Last Modified: Mon, 01 Dec 2025 20:06:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55257c3d032f819d9e4748c52ded91189a287550d89b352091a370beca2ba5b`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85942b89c334b57c1e4e2fe04e33640665135de4cf8a2d27d6a436c97fe1d9a0`  
		Last Modified: Mon, 01 Dec 2025 20:06:01 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a09f1c0c636c8f8267d5506ec8bbedf1a0fba433d3873c67e271bf583a6d60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a6b1ced3f2a40e081f12810dd8e801480fce3c7be1cae2bb55233f09a11d1`

```dockerfile
```

-	Layers:
	-	`sha256:51fa8da7b8dd1542e263e8e956d719d718aaf056a9e259fa5155c710fc4b0762`  
		Last Modified: Mon, 01 Dec 2025 22:50:18 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:5fcd6df6cb3aee2cc45eb9277bb382ca701badc83f590b0aabd1e10d0f40afbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:400907dae0e46f4e66a5da2587b698ecc5c952bcc57a6927f055affb169483a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228638783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3342638ee91c36aff149b1d07efc50d52c4042654d69d1f2c639a058f0543bae`
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
# Mon, 01 Dec 2025 20:04:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:04:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:04:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:04:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:04:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:04:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:05:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:05:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:05:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:05:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:05:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:05:21 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:05:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:05:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8cba820e4162b3066cd5f576620214a02239f91837e6c726ecdcea858b22b`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 7.6 MB (7598540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4217c0e232942cb5cb16a45e6e71576094748c0ceef05e12b49154b00d09af`  
		Last Modified: Mon, 01 Dec 2025 22:51:34 GMT  
		Size: 190.6 MB (190633415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d4425e61f161ae871b40462b3139ba4b7ac49ae62f5178257af79d60bd950`  
		Last Modified: Mon, 01 Dec 2025 20:06:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774b6dca825bcf7006168be347e7ddbd3b7118a852fa2073e1e3ffa28b5f5382`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 865.8 KB (865754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705cc2f178baaa750bf4919fc120c296bbfb297b77a3faf08dfeac83dfdba2ea`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ce21ce6d97ebc5d6ae1b8f71507fa59c50a62a5b5dc1e16a9e20c313b40d2`  
		Last Modified: Mon, 01 Dec 2025 20:06:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d25c625a633276da07ac12e84347c53f63e59a3b2fa6a08c4f474ededd04eb5`  
		Last Modified: Mon, 01 Dec 2025 20:06:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:88602181ece788e3066549ea0f1f0ded8263679f7cb6b7d450bbf2a503cf1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a332c3385b4acbf1a2c7210fdc968d9291fc2c41052ae5199aae7e57782eea`

```dockerfile
```

-	Layers:
	-	`sha256:7bd8c69cde986b1eabc72259f4cdda6783079992bc5ce2dd3852deaed06803a6`  
		Last Modified: Mon, 01 Dec 2025 22:50:53 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:780aa2240e58f768620951b47f88e127c595f51bb43f6206ea8b81c34e98f10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213458420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd323a8f97f32e2d3519c81b23d5fc0860545961bb4da9a2acb6d908ef2530b`
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
# Mon, 01 Dec 2025 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 01 Dec 2025 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 01 Dec 2025 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Mon, 01 Dec 2025 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 01 Dec 2025 20:05:50 GMT
ARG VERSION=25.8.12.129
# Mon, 01 Dec 2025 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 01 Dec 2025 20:06:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Dec 2025 20:06:20 GMT
ENV TZ=UTC
# Mon, 01 Dec 2025 20:06:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.12.129 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Dec 2025 20:06:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 01 Dec 2025 20:06:20 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 01 Dec 2025 20:06:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 01 Dec 2025 20:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63594f06979ec5b6ac5708128c6f4c8c5e949558123ccce2f7c7e22b8b30f75`  
		Last Modified: Mon, 01 Dec 2025 20:06:59 GMT  
		Size: 7.6 MB (7576742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4487a53362fe65c87e28b6725a38e9ce97b2afe8d38fca4976858f7042472`  
		Last Modified: Mon, 01 Dec 2025 22:51:27 GMT  
		Size: 177.6 MB (177627777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9188f96df6e213145ab134c0bc6c125f8a03509fb4303333eab8f92f7ba48`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e434244cd8a2941877cdd4356bcaf599bca499051d93aeab82ee06ad1fc49e1`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca91038b7f507b1dd7e99271b336106a4c6a2af3246388e326ff42bf4d4bc5`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c3c8c0cc4e1353985f77fb8111f8180eee06138276b0da73dfaacaa8e719a3`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0b1e5e73d7b9788eacc70bf649f7fe357bce8cd496a6a229ce6598347e37d`  
		Last Modified: Mon, 01 Dec 2025 20:06:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c81e7da5b896cb36c2b37093c464549801dc1ef0c99240656ba9f66fcef248b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba05a1970f5823facca0cf3058510191db9bce16e5acd09b6f91cf21134ad5be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0cde2d632cbd3711e951ea152c89a46d442a9802473a2cf50fb66cbcc1386`  
		Last Modified: Mon, 01 Dec 2025 22:50:56 GMT  
		Size: 26.3 KB (26272 bytes)  
		MIME: application/vnd.in-toto+json
