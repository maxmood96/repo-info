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
