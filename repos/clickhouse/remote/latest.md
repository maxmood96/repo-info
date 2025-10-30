## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:31de21589d0d2a7641492d645b53535efc35751fd36ca43929031cd012293af5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json
