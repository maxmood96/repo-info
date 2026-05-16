<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.23`](#clickhouse25823)
-	[`clickhouse:25.8.23-jammy`](#clickhouse25823-jammy)
-	[`clickhouse:25.8.23.13`](#clickhouse2582313)
-	[`clickhouse:25.8.23.13-jammy`](#clickhouse2582313-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.18`](#clickhouse26218)
-	[`clickhouse:26.2.18-jammy`](#clickhouse26218-jammy)
-	[`clickhouse:26.2.18.8`](#clickhouse262188)
-	[`clickhouse:26.2.18.8-jammy`](#clickhouse262188-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.10`](#clickhouse26310)
-	[`clickhouse:26.3.10-jammy`](#clickhouse26310-jammy)
-	[`clickhouse:26.3.10.62`](#clickhouse2631062)
-	[`clickhouse:26.3.10.62-jammy`](#clickhouse2631062-jammy)
-	[`clickhouse:26.4`](#clickhouse264)
-	[`clickhouse:26.4-jammy`](#clickhouse264-jammy)
-	[`clickhouse:26.4.2`](#clickhouse2642)
-	[`clickhouse:26.4.2-jammy`](#clickhouse2642-jammy)
-	[`clickhouse:26.4.2.10`](#clickhouse264210)
-	[`clickhouse:26.4.2.10-jammy`](#clickhouse264210-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23-jammy`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23.13`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23.13-jammy`

```console
$ docker pull clickhouse@sha256:813e04f3f188f8adba8fd08b51794d1f30e4822321774a322cef9ff9299b51fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23.13-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2e16a497bcfe584e2c4f58a027dbc145a6b8daeadee2c4c0ca9f5e1304e968cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d9a0505a50112269cd270cdb4b1a6613007329a8e67a577a682d7f9dd44ad`
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
# Fri, 15 May 2026 21:11:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:36 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:12:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:12:00 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963dada9f42401d3f359204937ae24905aa7e0df73ba8e2bea11f2491ea3998c`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 7.6 MB (7599257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f1466e30b573bb22b3de6b57d7f603368ce91228a30a1a950233a01655db3`  
		Last Modified: Fri, 15 May 2026 21:12:28 GMT  
		Size: 191.5 MB (191530595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893d980521543c6f097021f13012396ee3f4753aab80cb586b3d5288a288f3e`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6679ade1818297dca468c406951817ebdd7b5d092ea2b6769c555c3bb88ed`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c732fc4e2733025c77df9346281e772a08fed22f98dbb021d9097f0a892c7e`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0bdf18f8ee8a41381a117ee394a1feff3e6a5d1cf875a2aa9b05cb8d894eb`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243fe8c80f1c5764d8e0cf0ca939f369b71da7679fb939fdede61f1ec0fafbe`  
		Last Modified: Fri, 15 May 2026 21:12:24 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ce5d703ac2cb86364968ac130c3f41ba12b39c22ba45361143b3613786ffce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfc018709fb4388b0394f23f9696467935610f7fc35238f5a7586932d436bee`

```dockerfile
```

-	Layers:
	-	`sha256:61cca9e32b07c8f8d4ac4f1690f9265c8135eb43f71d86f9614fe31d93abab9b`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23.13-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec06428b797bf4b714999316a8c2999a7d16ec6594d9d5db9671797b578fa309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214756023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0560fbb48ec7d965325be6349d6f7d633ecadefd6582256ef4130fe9c30dadbd`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ce506443d4719764b571e4296459bdd2e58f9f3a212cc42c83d5405594853`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf7718970adf177ab5fa2be8a738438d3e6f518fc6bf6cabd7b2f2395f7db1`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 178.7 MB (178700434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf038f50ec23176d22c49fdbe6a3501500399451af756f72e3ae63ee404211`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a583439a6ef0d500ec903f2b63f5e819867e6abd83613827c137ced8dbfe4ad2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb1d3893e5de196d942db4d784a540cdf21898208b65f1bfb515f8910a6793`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f385f9a9e44c1bb8ed6e1d0021db3549978ffab34307f57b2f27a34a38d27d`  
		Last Modified: Fri, 15 May 2026 21:12:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fd87e4500cbdb6a00ccf9cfa577f54daa675033242fb4d718e6f18eaaedad5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203c3e69735d3fcea387a3ee3ccd4479caeb26b7686b0030dda6a399de43741`

```dockerfile
```

-	Layers:
	-	`sha256:6017cd513efe819764e61fde10f6cf69e4b9db13a15ece057f501cbfe7e29020`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18-jammy`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18.8`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18.8-jammy`

```console
$ docker pull clickhouse@sha256:5fa3b095f4257d490031a1800d3709bdcdcb5777e530e4934f99edea91acf0fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:97a6f644fbde2310d5ec6bbdc478f899ef6aee04c891a4bc0ab6ae08ba6978a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253840024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5bb854c4e3db2b811cfad7e1e3aa597df0079e43c5758a3f7513ccac5cba50`
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
# Fri, 15 May 2026 21:11:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:28 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:28 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f5624c7e684d4894c64524424277ec865e0b5e17137d6196fe42095f782c2`  
		Last Modified: Fri, 15 May 2026 21:12:13 GMT  
		Size: 7.6 MB (7599286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d9aef3d610026abe5b48346c389bde99bb7ecd6aaa91f60b32bdccbf819c1`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 215.6 MB (215634001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546de2f0e70e193e5861a2f5b2282f846be61dc2318a9c6a386051803cbe2bdb`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f244552c77f22f3f9e3ab1e870dd41b0a1fa85d7c52adc69be2d58eb84b4fdd`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428e1ee32ba55e7f73aa71868b27c64876012339fad058501716da2f37505a3`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65b018583f86b843e11c9b25438347525cdc91df05cc16392e0cda30464490`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844feb67aa98fda1f0e7f104ee7f9c015058c7cb8ace1b77ded5a039441496f9`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b018b6cfa06a05634bd46eacaa1a890e9bd9b72eaad6f397300db62acf7e1bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c415edaba3fa114bb4f6e3c67c3ff68af623d4e8f6ebc657cdd9637711877a5f`

```dockerfile
```

-	Layers:
	-	`sha256:59eb36a3ac10c3b4b24070f2ae86b751a87416c7fcd174954653f31515bd05c9`  
		Last Modified: Fri, 15 May 2026 21:12:12 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87fbfd1f6219a3de6632cd1e1f6d06080cf6245554ce6043ec7136c9ae9e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8638b8e6cb2289d732b7042074d0f982250c45281a5e0a61ae8076e4db779a69`
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
# Fri, 15 May 2026 21:11:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:23 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:23 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 21:11:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:53 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770354b8b698187e380d8ac49d5abb9f8264c395f9e9e985fb9fa63bc5acb74`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce1b8407fc24ead66f81a1a53257bba922c9578183e0666dc11d7a66d73a56`  
		Last Modified: Fri, 15 May 2026 21:12:22 GMT  
		Size: 201.5 MB (201451513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b46089d4165a2afc67f615932be50d5fb4f8959db36cb295084b6606e52e00`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0dd519e51cf0ebcb75d5bd74e1bddcb31a050143c5ed002193cf8786d45ed5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be58602c37044d15602be18b5f7c654ead1f402faf98444fc28c9ccd81ffd94`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e921f5d24de273451c5623b4d6dc8e7d077ae65b3f02f2e3be8e3be5c94592`  
		Last Modified: Fri, 15 May 2026 21:12:17 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0ff7e3d45e46d388a8b494f8486e22ba80006c03148f16898b948fba8c14f`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aee3d04e5e6554ef938fd38e9352d6ffdf6921e0856e37380dd927869506c0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57fd05d65245af6cace814a75ec27ab92663a71cc888037a9fbda4023c43778`

```dockerfile
```

-	Layers:
	-	`sha256:4bc8cd11c43c0e6212b638d71e5789466036b8fec9c51535eca6538decc36dd5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10.62`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10.62` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10.62` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10.62-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10.62-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10.62-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4-jammy`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2-jammy`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2.10`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2.10-jammy`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:5500cd56601d910aff2138e995ff5635ddfb8fa5e2ee0d86bec0b7336b11a6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:4b6206085e29fb51a2c4f0690082585c5e131ecff146505c18752d107b407385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189db40ea7dcd858b78ed2adbf568f5bb60a18f1a9b9da11cf3283079c65193`
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
# Fri, 15 May 2026 21:11:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:10 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:35 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660f5e3ea9f4adbe4c53f905abf301c41c69063b242eb4037f66d8a3baffea7`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 7.6 MB (7599269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bc9c52b77c39622ee8224248851f906b17da17fa8b0d50acc1028369016555`  
		Last Modified: Fri, 15 May 2026 21:12:06 GMT  
		Size: 218.9 MB (218919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418e507d974115cd92a39605d4ef8ee4250b622d0dbcaf130ac13da0826c092`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0d4069deb983db47b4e1de30c913d0d9bd11d2bc7932e240d4899329becfe`  
		Last Modified: Fri, 15 May 2026 21:12:01 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ea5707ace3b47f922c3c301a89929124d96e468e73d4ab95bed82f1b4d364`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a28ba87f4e778cbfeee38f44c73c0acc37bbb6c8ebaa6ea6c76f0715fb92d1`  
		Last Modified: Fri, 15 May 2026 21:12:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3042e39fa2fd100080a7fbf1a69a50929a4b73c8bf1625aa0a57d2dfba19e7`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:12fa1d73b1d5231ff7668aa552072bf0fa95d71b276449b49548490e671f6b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baf67648edfcc6adcd58c87bd6352a5e10d552826aee82d1c2d06713da338a2`

```dockerfile
```

-	Layers:
	-	`sha256:ca4f584046e8ce95bab99bd567e01220624ac4f11118829bdd6d134fe7252a47`  
		Last Modified: Fri, 15 May 2026 21:12:00 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f3f332403fa0dbc5798970f530898db537cb2f6a4ed9293ad532f4397543debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838d1ab1746c94911b690c3718945d9f3edd45a79482e4fbfa7d1855e8e08881`
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
# Fri, 15 May 2026 21:11:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:22 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:22 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 21:11:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:54 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d6fd2dd469d61ede0bb585fd88f4d75e3d53c9ed16ddba93bfd97a789e245`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 7.6 MB (7578906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6969a6112c8c8bd4d1516bb9ab03290e8026031934cf5c55da6f659f6befd8`  
		Last Modified: Fri, 15 May 2026 21:12:21 GMT  
		Size: 204.9 MB (204878412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a229a367480745069a5bc1263de86e819353e63b5182ddc3513be1956b11c3`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e3306725d7a38b3d3928fa6ebe4ac32353d470174fbcfcc45f2d87860aff5`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3185c656fe84b09015f02c162be0d7661a6165e8d6b038c248f6470868e37`  
		Last Modified: Fri, 15 May 2026 21:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299880ed7614c0e1b92f7ad8a74bf9937c96588527690a9cac5883fecac849d`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a5081be67caee1cd05044c599be1db2d328757629bc2ad94eaa72c09fce60`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eddbf3586c3b7285596928ea2fab0ad87cf7fc3e30eb72d51e7a86546a3eac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2352966d11c3f2c6609eb4605b3b7a5c70ed388b32cf444030fc713f4a7f3`

```dockerfile
```

-	Layers:
	-	`sha256:07e405c7b87cac019a9bd2634c827ddbc3b1d43e7cd4c40401f51518821ec278`  
		Last Modified: Fri, 15 May 2026 21:12:16 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json
