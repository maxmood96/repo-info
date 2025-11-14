## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:c9739650884bcc5dd109c283ce545b87d58c0f751880aa425170a59604aec341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f0d8c09cd53e9787cb3ee8f7e8e7cfde488fdddcb0b0502469b80b3b8a84c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2269ab9ff71a3eb770715c7a3fd75761efe8ef23a6c788abaa57f2e3cb78562`
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
# Thu, 13 Nov 2025 23:09:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:36 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:03 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd02d54aca9e4b5dc021fa7f9e576a07e5be62fc7ee172d0ed4137944cacc9`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316601fd9c34b60c5ca2605fa55d8290e2bd5ac69198cd0a53467a567f7fc83`  
		Last Modified: Fri, 14 Nov 2025 01:49:55 GMT  
		Size: 194.0 MB (193977827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39390138026777c687e3508ed8fd34055ace99ecec73f69c797cafd8492cc5`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276dfe45586cc645faa4c6655eebeeee38ea04261463b342d877bb60f895e787`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975ad1545a1b9982f545077922f5494e5c50dde1ed46614c6aa7b1ccac1dca1`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b39058858cb54734eaea1eb73e6efcc4ab04b4dc823c4d49ae39c219cd92e`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abed04583b3f8484627b7110037ce3ab26c7588a582f0da788ee9733c83ff42`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ae05d5e36eeccc46858a9c47b42e6578e2fdcb657160f8fc633a3969c05d158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d4c960d9c1b2ffe0e50ce35b612b69e231b9afad0c7f6da252c01c5a4f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:130306bcdc0b3daacdfe7da0deb2a61f1322af37824c618b9d715bde6aa88ba3`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:eeb67abeca6c00dd7fac755651c7ed2042118211e8ee5e999ba9cdfdf56aaa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601fbc006cdf774790f0afb3a7ab6d279f4acf3f6380c3ab0ff11a9bca50c9b`
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
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:58 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:09:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:09:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:09:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f5ce5c4571b4cd2464c78cbcd31672ad12226725a8e1232e8c3ef3620f9e0`  
		Last Modified: Fri, 14 Nov 2025 01:49:52 GMT  
		Size: 180.7 MB (180675112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8a51714ff93bb140e12b0158c088b6cde1651b653c1e455860479be6303b3`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87b3cb86dd50e65da599ed4a968edc62c5594830a198faad91aa3dcabcc814`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50b7ab24f69fdcd396dd7a078c175c8467d0556dbc8b3fcc5380d6706706d8`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd2bca9e63b0ebf70cbb92ffe0393da57cf1fb923a96941174aeb3097fcec6`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112adfbc3ee3dc6c7d4917a8ce15830879e6ca2aaeaeb47fa47375bc0c20b711`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:409797aa5d0365a362df23fc70f1d4ce92527bb13e6286b7c888e5248ab34776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf6e4289fb787eb33803b732451b0a765a8ddcc8f98c1a84d2f72a690e44f7`

```dockerfile
```

-	Layers:
	-	`sha256:d4f623fa03cf7b7f07af675778466cf0ce1e0569ca834dc8872842cbdd413a01`  
		Last Modified: Fri, 14 Nov 2025 01:49:27 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json
