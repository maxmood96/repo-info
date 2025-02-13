## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:114b90b999fbc52f96cc6500f11e4155a8265837da8554fc946a9849850479f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:614f3623ce61cc35fc802f88a5b87fbdec6f74e415457354c0eba6cfc33e87b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e643a00e2fe01d1778f90e7b6a9989a2dddf7e6e09b92fc9437c740f922c4d4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e971b047520974c8230021d6f58037c308e69ec52aa86b268409fb1488c7630`  
		Last Modified: Tue, 04 Feb 2025 08:15:12 GMT  
		Size: 7.1 MB (7147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431eed92df52a876033c3556d4769970c7ed827b68435067235f030164ae9ab`  
		Last Modified: Tue, 04 Feb 2025 09:45:09 GMT  
		Size: 148.3 MB (148318724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282701628944a8c7ed9fed5bf8c0bbe221c8104f3c50ee2f74ca09241de02e8`  
		Last Modified: Tue, 04 Feb 2025 09:28:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f362d62e6a2439305e3eaf466a07439d11e73f1b6f5e575d88ba94bb0adcad`  
		Last Modified: Tue, 04 Feb 2025 09:57:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca3b6e1c356821331a01f4f992b623903ca08a746b67744cc6598592db96f4`  
		Last Modified: Tue, 04 Feb 2025 09:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc3f0473cd0a8d3265599ce60df8ce4a6d004f33f7d0cd6b2c62b717beeb1a`  
		Last Modified: Tue, 04 Feb 2025 13:29:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d8618f6185f14eb71cf45b05cd76c5ffd3acbb63432e53d79758838886761`  
		Last Modified: Tue, 04 Feb 2025 09:57:46 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e11e3ddf694681284cc87eb819c2238fd5358335c8fd15fa3361cfa1b940131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05a37587143943915fc4d0dd868d2af5f6e23a0ebea0fb241259ece72f82bb5`

```dockerfile
```

-	Layers:
	-	`sha256:3f4bde278d014be13f9ddb61e2f8d965ece0054b98f617f44ff5e02a6417dee7`  
		Last Modified: Wed, 05 Feb 2025 13:13:09 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25db00e3d782f4ec46781003e5f5fd4172e3f0a67ee7b44160f55a007edd42b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176104181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78803e05ff68857629e0ab05e6fc097c647ae3a2a17ae18778c3b77e9c8e8f4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Jan 2025 12:29:00 GMT
ARG RELEASE
# Wed, 15 Jan 2025 12:29:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 12:29:00 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 12:29:00 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 12:29:00 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:29:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Jan 2025 12:29:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Jan 2025 12:29:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Jan 2025 12:29:00 GMT
ARG VERSION=24.12.3.47
# Wed, 15 Jan 2025 12:29:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:29:00 GMT
ENV TZ=UTC
# Wed, 15 Jan 2025 12:29:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.3.47 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Jan 2025 12:29:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Jan 2025 12:29:00 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Jan 2025 12:29:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Jan 2025 12:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd056c9792de4d65b4067be0104e80dc9e044a7993a4c91ccae9b92855307f`  
		Last Modified: Tue, 04 Feb 2025 14:12:53 GMT  
		Size: 7.1 MB (7121135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280c3f1da2ad99be4d13c11bd9ef4eb850b9141ae13b33fc1433596ef33e3755`  
		Last Modified: Tue, 04 Feb 2025 11:28:41 GMT  
		Size: 140.8 MB (140755301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd0f9aaa7b0741a865fd836e9457b06f867f717b91be035161e2da409d294e`  
		Last Modified: Tue, 04 Feb 2025 13:29:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779806710bd9c47daafa9a17f24e33b7b80dadd4972585e1d35ce821ebaf100`  
		Last Modified: Tue, 04 Feb 2025 12:19:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499a1ece5847243fbd9c9e623002f437c326854911fb0865337697fb6d1b274`  
		Last Modified: Tue, 04 Feb 2025 15:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781a6e97bbe4c4956f03bed727b1054acf45ece65018f68b5866fb8e624195b`  
		Last Modified: Tue, 04 Feb 2025 17:40:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5c1390d9a82af471e3057492e2d27c47138432d5f7c2e6148c15c551d8271`  
		Last Modified: Tue, 04 Feb 2025 20:26:25 GMT  
		Size: 3.1 KB (3148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5e5c32d6208b3255d1917517845ee0934957a16a4ee53051159bae3aa7cdd884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3bf829e90dd4204a0a8c1fff7b71b660fc435a6287c49b556c87109bf3a768`

```dockerfile
```

-	Layers:
	-	`sha256:fb45662c55da5245303440dd0f01b0fb1c73ca7b7614e4acb16c4a3898eff3c3`  
		Last Modified: Thu, 06 Feb 2025 02:07:45 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json
