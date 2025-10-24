## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
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
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json
