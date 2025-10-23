## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:5ff4706707afcdccfc4edd08b2c5d18b084317b2d5c9809e1b49556246d8840d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:84fd81d298f84c29536442cd4a2aef2db9b94d22cd653dfc3b40916bd14dcf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228816946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a003c9aa6fe037ce6bc43fa8dacc4b7ad9e8c29198a25c86e13784eaad89c290`
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
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.9.3.48
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.3.48 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.3.48 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.3.48 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.3.48 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08d4092b78718d94506a9f15a0f06b49ce6e4fc6a119f0500dec8ffe1157997`  
		Last Modified: Thu, 09 Oct 2025 18:50:14 GMT  
		Size: 190.8 MB (190811710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4d09fb0126fd1a5b8592b797ed084de116b0cd62251524b985ed11aa0f4a79`  
		Last Modified: Thu, 09 Oct 2025 18:04:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a06361f60f8414b1e37dfbe7beaa38779e0618c5e4c8dfd24436ecee78f320`  
		Last Modified: Thu, 09 Oct 2025 18:04:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7b45365a8b2bb5c2fd91c0bec6913ccb7969afdb1bac83cb548bed904899ec`  
		Last Modified: Thu, 09 Oct 2025 18:04:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46801521c3f56b0ff49fb83714163c3a592a95576a837b60b86f81408cfdd8b7`  
		Last Modified: Thu, 09 Oct 2025 18:04:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9d20d726c6ba2ba0c700a1d3bc7cd89b9d1bcc146c05d11c48ef3f727136e`  
		Last Modified: Thu, 09 Oct 2025 18:04:05 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78bd1595cd32e3eb6910d8ed0ed11789b087b8765bd631eadd67ab15ecb65bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b934eebccf8d18dc6e27c030270b652ee2988241418fafd989407e0c294f5caf`

```dockerfile
```

-	Layers:
	-	`sha256:89a5bbe8b2f16a9068b11d60e5a0f00f2b770ed5f6c6d6fd80a5c591694383ed`  
		Last Modified: Thu, 09 Oct 2025 18:49:49 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

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

### `clickhouse:jammy` - unknown; unknown

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
