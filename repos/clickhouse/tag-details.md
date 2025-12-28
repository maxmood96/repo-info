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
-	[`clickhouse:25.11.5`](#clickhouse25115)
-	[`clickhouse:25.11.5-jammy`](#clickhouse25115-jammy)
-	[`clickhouse:25.11.5.8`](#clickhouse251158)
-	[`clickhouse:25.11.5.8-jammy`](#clickhouse251158-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.1`](#clickhouse25121)
-	[`clickhouse:25.12.1-jammy`](#clickhouse25121-jammy)
-	[`clickhouse:25.12.1.649`](#clickhouse25121649)
-	[`clickhouse:25.12.1.649-jammy`](#clickhouse25121649-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.11`](#clickhouse25311)
-	[`clickhouse:25.3.11-jammy`](#clickhouse25311-jammy)
-	[`clickhouse:25.3.11.20`](#clickhouse2531120)
-	[`clickhouse:25.3.11.20-jammy`](#clickhouse2531120-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.13`](#clickhouse25813)
-	[`clickhouse:25.8.13-jammy`](#clickhouse25813-jammy)
-	[`clickhouse:25.8.13.73`](#clickhouse2581373)
-	[`clickhouse:25.8.13.73-jammy`](#clickhouse2581373-jammy)
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
$ docker pull clickhouse@sha256:c88edfe07d7945f3ed336fbc6fe1b12ba40eec3edd0d70322a1d64dc06b617a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:f55d3059d1c617aa46493162eb3f2a21a150bc1bb4d8cd33f7e6ab31b01d371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233887911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaef05cdea092bc684cbd3d676100a02e300ddcddcd17f7df32799a3bc5af53`
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
# Thu, 18 Dec 2025 19:23:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:23:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:23:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:23:24 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:23:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:23:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:23:52 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:23:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:23:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:23:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff67eb215d524a605eb9efcc5039ea591a49ee3eef4e66d37f4637e2dbc59450`  
		Last Modified: Thu, 18 Dec 2025 19:24:28 GMT  
		Size: 7.6 MB (7598557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d283361e7830b58a308d91b51a039ac62779d43f34f59deb6d4b72dbbc51b71`  
		Last Modified: Thu, 18 Dec 2025 22:50:09 GMT  
		Size: 195.9 MB (195882510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510176455abc343f3d1721eaa8f7e0b8d71bb1bcf609ff2b562c1134e7615bed`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a900c1e1125b66adad26ac2910d2ebaa9e2ef88b905641015ba167bbb19749cf`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95c6d7a870ba9def922a09e44c3201377b1526217f08c7c9d03e7a780f9a192`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa95443635767205ff71ee8c7227b197dbc4893025729298ecb9a1fe251874`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385199fdd1e4b5d5e56237586c7ed6b92b65ced6e664885b31cad24c28c6def`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35eaec7fd6afe02b002bfce3f59ae0718eeb31e16d1d4cdd02f34734d91b7b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6b81ad3ea719b2bb7de4decc13aa2499bb87191baba93f0e582381c7eecbf3`

```dockerfile
```

-	Layers:
	-	`sha256:d18d0c4a5c92fb1a73e3e69e4acf4662259da5f5c504016c2bf9fdcee1d97abb`  
		Last Modified: Thu, 18 Dec 2025 22:49:27 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:264ff776113574a81ba044e55e715b047998eede2e7b5c0c12d322cbaf59b68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218814818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccddc0a863096d406a359f25ac4c79f6883b893a61e9d2f9ef33355387b8b1bf`
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
# Thu, 18 Dec 2025 19:20:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:20:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:20:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:20:45 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:20:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:21:12 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:21:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:21:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba310e3441eb3bc6f04c79fdf3fd00639bc1d4327330abfb81792d3d27308d2a`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 7.6 MB (7576793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edea552b087f106b458f401dad584048a27ad6b2c5eb6f16b123cf52cb6144b`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 183.0 MB (182984105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5645892c01c36540de2aa89aae4a0449b386729cfa57a03fef909f086e9c0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331499aed8f912bba693b85fbccaa84941c5101d7be933c5aa5b76a0dc271e0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095be2403e664d4f64de972f0b0a8dfc858494e89e09f9a3b5a173c7c4560c7`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519cf0d8cb1165b2daca9aa11f5101d6afa81d30008de2e15321809169673521`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae99bfb41d2c2fd8e3ba0b01e83f5cfc42a79721581886945ae28a0a8e4d5b`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd7298281972be8595f3f5a85613c412ba89a952285f70ad8e8dee5a90484a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fedde820601e90ecc5c587d11b3e1665068cf60615a0aeceb68da291440b3a3`

```dockerfile
```

-	Layers:
	-	`sha256:ed470a0fecb9ae7db5e75ac8bb2cca4999778877ced153a26fdeab3d8c68255e`  
		Last Modified: Thu, 18 Dec 2025 22:49:31 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:c88edfe07d7945f3ed336fbc6fe1b12ba40eec3edd0d70322a1d64dc06b617a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f55d3059d1c617aa46493162eb3f2a21a150bc1bb4d8cd33f7e6ab31b01d371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233887911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaef05cdea092bc684cbd3d676100a02e300ddcddcd17f7df32799a3bc5af53`
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
# Thu, 18 Dec 2025 19:23:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:23:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:23:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:23:24 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:23:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:23:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:23:52 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:23:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:23:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:23:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff67eb215d524a605eb9efcc5039ea591a49ee3eef4e66d37f4637e2dbc59450`  
		Last Modified: Thu, 18 Dec 2025 19:24:28 GMT  
		Size: 7.6 MB (7598557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d283361e7830b58a308d91b51a039ac62779d43f34f59deb6d4b72dbbc51b71`  
		Last Modified: Thu, 18 Dec 2025 22:50:09 GMT  
		Size: 195.9 MB (195882510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510176455abc343f3d1721eaa8f7e0b8d71bb1bcf609ff2b562c1134e7615bed`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a900c1e1125b66adad26ac2910d2ebaa9e2ef88b905641015ba167bbb19749cf`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95c6d7a870ba9def922a09e44c3201377b1526217f08c7c9d03e7a780f9a192`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa95443635767205ff71ee8c7227b197dbc4893025729298ecb9a1fe251874`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385199fdd1e4b5d5e56237586c7ed6b92b65ced6e664885b31cad24c28c6def`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35eaec7fd6afe02b002bfce3f59ae0718eeb31e16d1d4cdd02f34734d91b7b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6b81ad3ea719b2bb7de4decc13aa2499bb87191baba93f0e582381c7eecbf3`

```dockerfile
```

-	Layers:
	-	`sha256:d18d0c4a5c92fb1a73e3e69e4acf4662259da5f5c504016c2bf9fdcee1d97abb`  
		Last Modified: Thu, 18 Dec 2025 22:49:27 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:264ff776113574a81ba044e55e715b047998eede2e7b5c0c12d322cbaf59b68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218814818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccddc0a863096d406a359f25ac4c79f6883b893a61e9d2f9ef33355387b8b1bf`
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
# Thu, 18 Dec 2025 19:20:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:20:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:20:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:20:45 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:20:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:21:12 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:21:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:21:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba310e3441eb3bc6f04c79fdf3fd00639bc1d4327330abfb81792d3d27308d2a`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 7.6 MB (7576793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edea552b087f106b458f401dad584048a27ad6b2c5eb6f16b123cf52cb6144b`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 183.0 MB (182984105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5645892c01c36540de2aa89aae4a0449b386729cfa57a03fef909f086e9c0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331499aed8f912bba693b85fbccaa84941c5101d7be933c5aa5b76a0dc271e0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095be2403e664d4f64de972f0b0a8dfc858494e89e09f9a3b5a173c7c4560c7`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519cf0d8cb1165b2daca9aa11f5101d6afa81d30008de2e15321809169673521`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae99bfb41d2c2fd8e3ba0b01e83f5cfc42a79721581886945ae28a0a8e4d5b`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd7298281972be8595f3f5a85613c412ba89a952285f70ad8e8dee5a90484a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fedde820601e90ecc5c587d11b3e1665068cf60615a0aeceb68da291440b3a3`

```dockerfile
```

-	Layers:
	-	`sha256:ed470a0fecb9ae7db5e75ac8bb2cca4999778877ced153a26fdeab3d8c68255e`  
		Last Modified: Thu, 18 Dec 2025 22:49:31 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.5`

**does not exist** (yet?)

## `clickhouse:25.11.5-jammy`

**does not exist** (yet?)

## `clickhouse:25.11.5.8`

**does not exist** (yet?)

## `clickhouse:25.11.5.8-jammy`

**does not exist** (yet?)

## `clickhouse:25.12`

**does not exist** (yet?)

## `clickhouse:25.12-jammy`

**does not exist** (yet?)

## `clickhouse:25.12.1`

**does not exist** (yet?)

## `clickhouse:25.12.1-jammy`

**does not exist** (yet?)

## `clickhouse:25.12.1.649`

**does not exist** (yet?)

## `clickhouse:25.12.1.649-jammy`

**does not exist** (yet?)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:5190279a99df51ff27becb35816afcb40d3209897e946ab0fe778e252ff187cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:cffc81c2fb698e97e6ad01dbbedb4b180654083128265c9bbbe14ce6ae315c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206300116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb39f74da38e3be1bfef5b410d6bf97e2f7195b817e83c9f6942d477a1dfbe4`
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
# Thu, 11 Dec 2025 19:35:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Dec 2025 19:35:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Dec 2025 19:35:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:35:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Dec 2025 19:35:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Dec 2025 19:35:36 GMT
ARG VERSION=25.3.10.19
# Thu, 11 Dec 2025 19:35:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Dec 2025 19:36:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:36:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:36:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Dec 2025 19:36:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Dec 2025 19:36:03 GMT
ENV TZ=UTC
# Thu, 11 Dec 2025 19:36:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Dec 2025 19:36:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Dec 2025 19:36:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Dec 2025 19:36:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70549f85491cd8a97f54d6d890c12fad35feea5e48ddf23716c0f43bf2dfea5e`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 7.2 MB (7151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f562a65011ceb5b904617b79636f3210479edd9b1abe0f61640573d9f531ee0`  
		Last Modified: Thu, 11 Dec 2025 19:36:51 GMT  
		Size: 168.7 MB (168741349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65d96e669f0f22cdedd7fe784529f38e6b8cf559c4f639f6fa47094c4138d4`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feb6d07263cb16ce12d97be3fa924f14629873d1f265961bf4d53a1ee578231`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc04867e98a65fe0508fd510b5f93f788c5700be458bc3f75bf31f719b1a045`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5ed7af6ee05e76e457a9a37d7baed57a675d57763a04ff2c1f3cb67cf747af`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca30d9b55994e93c786f4f7810dd4f6e55ad58b363b91cad7a2a7b772d64a0d`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cabd08ba34146ca1420fe659bc1e311f830c74b21e01b76b594ce77a557de728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9ebecb71be6b6d76fc35601f0a7d502624b69a9e44fcb50c7e22ebd29400ee`

```dockerfile
```

-	Layers:
	-	`sha256:92d9f243e86bf8a9970a11364de2efa2e950b42025617f3faa96f13b1cfd004b`  
		Last Modified: Thu, 11 Dec 2025 22:49:26 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8c2ebee3d8a4bcb8210bfbb6e3ac08ff344a2bff3dff9acef4911be309cd9620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193785701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742967e6942932ba7c0b1c4ded1009f7db7a2fa63273173a3a5a4fac9572bd30`
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
# Thu, 11 Dec 2025 19:30:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Dec 2025 19:30:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Dec 2025 19:30:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:30:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Dec 2025 19:30:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Dec 2025 19:30:13 GMT
ARG VERSION=25.3.10.19
# Thu, 11 Dec 2025 19:30:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Dec 2025 19:30:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:30:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:30:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Dec 2025 19:30:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Dec 2025 19:30:39 GMT
ENV TZ=UTC
# Thu, 11 Dec 2025 19:30:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Dec 2025 19:30:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Dec 2025 19:30:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Dec 2025 19:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df27e3541ddc889bb74aaf55d4b6fd647bddac864165b203a6af5d3d6f57d2`  
		Last Modified: Thu, 11 Dec 2025 19:31:29 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc43db1007c7cc3fe95cfbaa9e49bf4c0f04bab7a380a86fac898fb100e7496`  
		Last Modified: Thu, 11 Dec 2025 19:32:33 GMT  
		Size: 158.4 MB (158404333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c632d14711a0c3b0d0bae2ec6b19e756a9681a54150d01e9720218edeed762`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a7c6d952f58d260ed6d9b97f186758396f90d2481ddaef6dbe1b9678ecbafe`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f010b97ee43fe63c94c3f7aad9b2c438fca3204bb0d4e4e3b27295809ec3895`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a9db7aebfd37892317eb55d6a7321874b38e9328e674ac3167a5f038ef00d`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7d05066264d4f62246a15f457ff8663628a5fa1f99e5b816197f314360098e`  
		Last Modified: Thu, 11 Dec 2025 19:31:28 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9c736c19bf45a909e1a3ec093734514a2b379a75257f90a89ce917d198b262b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ee736e6d578f9fd2fa88b2b357934bd2f44a23b39796b7f885a3db96d62543`

```dockerfile
```

-	Layers:
	-	`sha256:bd03b5a3ed55bd93c129da7a9272d171060fe9ec7a5763f7d93cf353736ef86b`  
		Last Modified: Thu, 11 Dec 2025 22:49:29 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:5190279a99df51ff27becb35816afcb40d3209897e946ab0fe778e252ff187cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:cffc81c2fb698e97e6ad01dbbedb4b180654083128265c9bbbe14ce6ae315c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206300116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb39f74da38e3be1bfef5b410d6bf97e2f7195b817e83c9f6942d477a1dfbe4`
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
# Thu, 11 Dec 2025 19:35:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Dec 2025 19:35:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Dec 2025 19:35:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:35:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Dec 2025 19:35:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Dec 2025 19:35:36 GMT
ARG VERSION=25.3.10.19
# Thu, 11 Dec 2025 19:35:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Dec 2025 19:36:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:36:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:36:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Dec 2025 19:36:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Dec 2025 19:36:03 GMT
ENV TZ=UTC
# Thu, 11 Dec 2025 19:36:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 19:36:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Dec 2025 19:36:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Dec 2025 19:36:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Dec 2025 19:36:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70549f85491cd8a97f54d6d890c12fad35feea5e48ddf23716c0f43bf2dfea5e`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 7.2 MB (7151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f562a65011ceb5b904617b79636f3210479edd9b1abe0f61640573d9f531ee0`  
		Last Modified: Thu, 11 Dec 2025 19:36:51 GMT  
		Size: 168.7 MB (168741349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65d96e669f0f22cdedd7fe784529f38e6b8cf559c4f639f6fa47094c4138d4`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feb6d07263cb16ce12d97be3fa924f14629873d1f265961bf4d53a1ee578231`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc04867e98a65fe0508fd510b5f93f788c5700be458bc3f75bf31f719b1a045`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5ed7af6ee05e76e457a9a37d7baed57a675d57763a04ff2c1f3cb67cf747af`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca30d9b55994e93c786f4f7810dd4f6e55ad58b363b91cad7a2a7b772d64a0d`  
		Last Modified: Thu, 11 Dec 2025 19:36:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cabd08ba34146ca1420fe659bc1e311f830c74b21e01b76b594ce77a557de728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9ebecb71be6b6d76fc35601f0a7d502624b69a9e44fcb50c7e22ebd29400ee`

```dockerfile
```

-	Layers:
	-	`sha256:92d9f243e86bf8a9970a11364de2efa2e950b42025617f3faa96f13b1cfd004b`  
		Last Modified: Thu, 11 Dec 2025 22:49:26 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8c2ebee3d8a4bcb8210bfbb6e3ac08ff344a2bff3dff9acef4911be309cd9620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193785701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742967e6942932ba7c0b1c4ded1009f7db7a2fa63273173a3a5a4fac9572bd30`
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
# Thu, 11 Dec 2025 19:30:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Dec 2025 19:30:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Dec 2025 19:30:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:30:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Dec 2025 19:30:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Dec 2025 19:30:13 GMT
ARG VERSION=25.3.10.19
# Thu, 11 Dec 2025 19:30:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Dec 2025 19:30:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:30:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Dec 2025 19:30:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Dec 2025 19:30:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Dec 2025 19:30:39 GMT
ENV TZ=UTC
# Thu, 11 Dec 2025 19:30:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.10.19 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 19:30:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Dec 2025 19:30:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Dec 2025 19:30:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Dec 2025 19:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df27e3541ddc889bb74aaf55d4b6fd647bddac864165b203a6af5d3d6f57d2`  
		Last Modified: Thu, 11 Dec 2025 19:31:29 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc43db1007c7cc3fe95cfbaa9e49bf4c0f04bab7a380a86fac898fb100e7496`  
		Last Modified: Thu, 11 Dec 2025 19:32:33 GMT  
		Size: 158.4 MB (158404333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c632d14711a0c3b0d0bae2ec6b19e756a9681a54150d01e9720218edeed762`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a7c6d952f58d260ed6d9b97f186758396f90d2481ddaef6dbe1b9678ecbafe`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f010b97ee43fe63c94c3f7aad9b2c438fca3204bb0d4e4e3b27295809ec3895`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a9db7aebfd37892317eb55d6a7321874b38e9328e674ac3167a5f038ef00d`  
		Last Modified: Thu, 11 Dec 2025 19:31:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7d05066264d4f62246a15f457ff8663628a5fa1f99e5b816197f314360098e`  
		Last Modified: Thu, 11 Dec 2025 19:31:28 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9c736c19bf45a909e1a3ec093734514a2b379a75257f90a89ce917d198b262b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ee736e6d578f9fd2fa88b2b357934bd2f44a23b39796b7f885a3db96d62543`

```dockerfile
```

-	Layers:
	-	`sha256:bd03b5a3ed55bd93c129da7a9272d171060fe9ec7a5763f7d93cf353736ef86b`  
		Last Modified: Thu, 11 Dec 2025 22:49:29 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.11`

**does not exist** (yet?)

## `clickhouse:25.3.11-jammy`

**does not exist** (yet?)

## `clickhouse:25.3.11.20`

**does not exist** (yet?)

## `clickhouse:25.3.11.20-jammy`

**does not exist** (yet?)

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
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
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
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
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
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
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
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
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

## `clickhouse:25.8.13`

**does not exist** (yet?)

## `clickhouse:25.8.13-jammy`

**does not exist** (yet?)

## `clickhouse:25.8.13.73`

**does not exist** (yet?)

## `clickhouse:25.8.13.73-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:c88edfe07d7945f3ed336fbc6fe1b12ba40eec3edd0d70322a1d64dc06b617a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f55d3059d1c617aa46493162eb3f2a21a150bc1bb4d8cd33f7e6ab31b01d371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233887911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaef05cdea092bc684cbd3d676100a02e300ddcddcd17f7df32799a3bc5af53`
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
# Thu, 18 Dec 2025 19:23:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:23:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:23:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:23:24 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:23:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:23:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:23:52 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:23:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:23:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:23:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff67eb215d524a605eb9efcc5039ea591a49ee3eef4e66d37f4637e2dbc59450`  
		Last Modified: Thu, 18 Dec 2025 19:24:28 GMT  
		Size: 7.6 MB (7598557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d283361e7830b58a308d91b51a039ac62779d43f34f59deb6d4b72dbbc51b71`  
		Last Modified: Thu, 18 Dec 2025 22:50:09 GMT  
		Size: 195.9 MB (195882510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510176455abc343f3d1721eaa8f7e0b8d71bb1bcf609ff2b562c1134e7615bed`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a900c1e1125b66adad26ac2910d2ebaa9e2ef88b905641015ba167bbb19749cf`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95c6d7a870ba9def922a09e44c3201377b1526217f08c7c9d03e7a780f9a192`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa95443635767205ff71ee8c7227b197dbc4893025729298ecb9a1fe251874`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385199fdd1e4b5d5e56237586c7ed6b92b65ced6e664885b31cad24c28c6def`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35eaec7fd6afe02b002bfce3f59ae0718eeb31e16d1d4cdd02f34734d91b7b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6b81ad3ea719b2bb7de4decc13aa2499bb87191baba93f0e582381c7eecbf3`

```dockerfile
```

-	Layers:
	-	`sha256:d18d0c4a5c92fb1a73e3e69e4acf4662259da5f5c504016c2bf9fdcee1d97abb`  
		Last Modified: Thu, 18 Dec 2025 22:49:27 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:264ff776113574a81ba044e55e715b047998eede2e7b5c0c12d322cbaf59b68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218814818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccddc0a863096d406a359f25ac4c79f6883b893a61e9d2f9ef33355387b8b1bf`
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
# Thu, 18 Dec 2025 19:20:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:20:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:20:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:20:45 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:20:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:21:12 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:21:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:21:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba310e3441eb3bc6f04c79fdf3fd00639bc1d4327330abfb81792d3d27308d2a`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 7.6 MB (7576793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edea552b087f106b458f401dad584048a27ad6b2c5eb6f16b123cf52cb6144b`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 183.0 MB (182984105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5645892c01c36540de2aa89aae4a0449b386729cfa57a03fef909f086e9c0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331499aed8f912bba693b85fbccaa84941c5101d7be933c5aa5b76a0dc271e0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095be2403e664d4f64de972f0b0a8dfc858494e89e09f9a3b5a173c7c4560c7`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519cf0d8cb1165b2daca9aa11f5101d6afa81d30008de2e15321809169673521`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae99bfb41d2c2fd8e3ba0b01e83f5cfc42a79721581886945ae28a0a8e4d5b`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd7298281972be8595f3f5a85613c412ba89a952285f70ad8e8dee5a90484a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fedde820601e90ecc5c587d11b3e1665068cf60615a0aeceb68da291440b3a3`

```dockerfile
```

-	Layers:
	-	`sha256:ed470a0fecb9ae7db5e75ac8bb2cca4999778877ced153a26fdeab3d8c68255e`  
		Last Modified: Thu, 18 Dec 2025 22:49:31 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:c88edfe07d7945f3ed336fbc6fe1b12ba40eec3edd0d70322a1d64dc06b617a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:f55d3059d1c617aa46493162eb3f2a21a150bc1bb4d8cd33f7e6ab31b01d371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233887911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaef05cdea092bc684cbd3d676100a02e300ddcddcd17f7df32799a3bc5af53`
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
# Thu, 18 Dec 2025 19:23:24 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:23:24 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:23:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:23:24 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:23:24 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:23:24 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:23:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:23:52 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:23:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:23:52 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:23:52 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:23:52 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:23:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff67eb215d524a605eb9efcc5039ea591a49ee3eef4e66d37f4637e2dbc59450`  
		Last Modified: Thu, 18 Dec 2025 19:24:28 GMT  
		Size: 7.6 MB (7598557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d283361e7830b58a308d91b51a039ac62779d43f34f59deb6d4b72dbbc51b71`  
		Last Modified: Thu, 18 Dec 2025 22:50:09 GMT  
		Size: 195.9 MB (195882510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510176455abc343f3d1721eaa8f7e0b8d71bb1bcf609ff2b562c1134e7615bed`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a900c1e1125b66adad26ac2910d2ebaa9e2ef88b905641015ba167bbb19749cf`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95c6d7a870ba9def922a09e44c3201377b1526217f08c7c9d03e7a780f9a192`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa95443635767205ff71ee8c7227b197dbc4893025729298ecb9a1fe251874`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385199fdd1e4b5d5e56237586c7ed6b92b65ced6e664885b31cad24c28c6def`  
		Last Modified: Thu, 18 Dec 2025 19:24:27 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35eaec7fd6afe02b002bfce3f59ae0718eeb31e16d1d4cdd02f34734d91b7b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6b81ad3ea719b2bb7de4decc13aa2499bb87191baba93f0e582381c7eecbf3`

```dockerfile
```

-	Layers:
	-	`sha256:d18d0c4a5c92fb1a73e3e69e4acf4662259da5f5c504016c2bf9fdcee1d97abb`  
		Last Modified: Thu, 18 Dec 2025 22:49:27 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:264ff776113574a81ba044e55e715b047998eede2e7b5c0c12d322cbaf59b68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218814818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccddc0a863096d406a359f25ac4c79f6883b893a61e9d2f9ef33355387b8b1bf`
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
# Thu, 18 Dec 2025 19:20:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Dec 2025 19:20:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Dec 2025 19:20:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Dec 2025 19:20:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Dec 2025 19:20:45 GMT
ARG VERSION=25.11.3.54
# Thu, 18 Dec 2025 19:20:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Dec 2025 19:21:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Dec 2025 19:21:12 GMT
ENV TZ=UTC
# Thu, 18 Dec 2025 19:21:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.3.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Dec 2025 19:21:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Dec 2025 19:21:13 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Dec 2025 19:21:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Dec 2025 19:21:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba310e3441eb3bc6f04c79fdf3fd00639bc1d4327330abfb81792d3d27308d2a`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 7.6 MB (7576793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edea552b087f106b458f401dad584048a27ad6b2c5eb6f16b123cf52cb6144b`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 183.0 MB (182984105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5645892c01c36540de2aa89aae4a0449b386729cfa57a03fef909f086e9c0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d331499aed8f912bba693b85fbccaa84941c5101d7be933c5aa5b76a0dc271e0`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3095be2403e664d4f64de972f0b0a8dfc858494e89e09f9a3b5a173c7c4560c7`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519cf0d8cb1165b2daca9aa11f5101d6afa81d30008de2e15321809169673521`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae99bfb41d2c2fd8e3ba0b01e83f5cfc42a79721581886945ae28a0a8e4d5b`  
		Last Modified: Thu, 18 Dec 2025 19:21:44 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd7298281972be8595f3f5a85613c412ba89a952285f70ad8e8dee5a90484a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fedde820601e90ecc5c587d11b3e1665068cf60615a0aeceb68da291440b3a3`

```dockerfile
```

-	Layers:
	-	`sha256:ed470a0fecb9ae7db5e75ac8bb2cca4999778877ced153a26fdeab3d8c68255e`  
		Last Modified: Thu, 18 Dec 2025 22:49:31 GMT  
		Size: 26.3 KB (26259 bytes)  
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
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
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
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
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
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
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
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
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
