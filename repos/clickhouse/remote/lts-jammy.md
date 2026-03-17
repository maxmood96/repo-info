## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json
