## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json
