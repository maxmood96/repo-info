## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json
