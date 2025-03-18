## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:a7374f29756e0e0c411bdb17dd60847dc3027b493cdbc8d2677c23a3a4692e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8c6978ba7c96a19335334b4c320aa0c99ab4ca15bb27c2455181cec18755b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cf4e799ec5f8a0c76c5186a064ceeda2814079339b145b0e25e5e6f5f2181`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5bb527330c4e88819c6d653d183929821401a4f16c62f8d5ae94e13657bd8`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 7.1 MB (7146955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b87611b20a20a4ebb94f1ca9c604da9b9b73ce98b18879d85ae33c727b3692`  
		Last Modified: Tue, 18 Mar 2025 18:01:59 GMT  
		Size: 163.5 MB (163483483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5969b3a5318afac96f8b1742456f9c714581eb1994b4b04a2463b2bb3dea9`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed87cf4b546f7816f90225ad967a5a40493970de9c779761c9e6a5afe588d86`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5972b64be71b578671907b675436384d061cc495de50025426eb1edbfb81e3a`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38d5e9fbfe681dfc50df314ac9227cdf8207d45551d2577dfd46d28b29f7a7`  
		Last Modified: Tue, 18 Mar 2025 18:01:57 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84a57c39a08ea55aa02d6e5e7318562206304d5639f6d2eed33082b13c832d0`  
		Last Modified: Tue, 18 Mar 2025 18:01:58 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:65cfb0e6be544940fa173785f643a7f86626efd51673c65045ac944c63b8fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed76ac3f47c595542af0f08659ae7fa75996049d4030948a8eb2779aeb8a43f`

```dockerfile
```

-	Layers:
	-	`sha256:afeeb8e5eadf66729188a37f76dae2aa6a10007999c673e18ef15021d5774741`  
		Last Modified: Tue, 18 Mar 2025 18:01:56 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:27:53 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 00:27:56 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:27:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:27:53 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:27:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:27:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:27:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 00:27:52 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json
