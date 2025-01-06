## `clickhouse:focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json
