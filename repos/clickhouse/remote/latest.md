## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json
