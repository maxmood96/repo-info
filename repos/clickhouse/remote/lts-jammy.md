## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json
