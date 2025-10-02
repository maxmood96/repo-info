<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.6`](#clickhouse2536)
-	[`clickhouse:25.3.6-jammy`](#clickhouse2536-jammy)
-	[`clickhouse:25.3.6.56`](#clickhouse253656)
-	[`clickhouse:25.3.6.56-jammy`](#clickhouse253656-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.7`](#clickhouse2577)
-	[`clickhouse:25.7.7-jammy`](#clickhouse2577-jammy)
-	[`clickhouse:25.7.7.68`](#clickhouse257768)
-	[`clickhouse:25.7.7.68-jammy`](#clickhouse257768-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.8`](#clickhouse2588)
-	[`clickhouse:25.8.8-jammy`](#clickhouse2588-jammy)
-	[`clickhouse:25.8.8.26`](#clickhouse258826)
-	[`clickhouse:25.8.8.26-jammy`](#clickhouse258826-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.2`](#clickhouse2592)
-	[`clickhouse:25.9.2-jammy`](#clickhouse2592-jammy)
-	[`clickhouse:25.9.2.1`](#clickhouse25921)
-	[`clickhouse:25.9.2.1-jammy`](#clickhouse25921-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6-jammy`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56-jammy`

```console
$ docker pull clickhouse@sha256:9bb4fa911f507f8599e41667fed553a09846be18eca01739781c363f9c2eba15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:995d51973a11ebd45b4b2923197b64d7be58419a194fc2fe27f62ab5e4ace4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f520afe8aedae117c2a35948adaf56d8220e7bfa580dfc7a4d79fe91e3a01`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020f7905cfe571cb026cd5783650ed5910e69dded4a78a6d46a0a991ec96c16`  
		Last Modified: Thu, 02 Oct 2025 06:49:23 GMT  
		Size: 7.2 MB (7151480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf1cc3d0d3a7b95b2d9d45d321dffaa79d6f70c804afc59341c45364c5d4b`  
		Last Modified: Thu, 02 Oct 2025 06:49:33 GMT  
		Size: 167.9 MB (167873549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6749065c967992c81886370a8d7802bf94ffa4d4de59a4cacc01f3dc66e46b01`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d02912112282a8d1a6564a77fa160916a4143025e821bfea93e314439d79ce`  
		Last Modified: Thu, 02 Oct 2025 05:24:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db664aeeeb74c7cf5fab5f2f1ad3fdab5931fbeb65fb7e11b5d0920fed92d38e`  
		Last Modified: Thu, 02 Oct 2025 05:24:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed2dfaf61fc0e38ad8e12cc750239109dda9bb22ed278c4eef98fca66a0b1f`  
		Last Modified: Thu, 02 Oct 2025 05:24:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefde5f186f704847eaebc796016b7793daa056d0c67df1ab57adb1cbea2cbaf`  
		Last Modified: Thu, 02 Oct 2025 05:24:56 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:13d2a601a2de421a5281c5d8477892319a05923e9d5eb109a5284181d79d6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1228b1cae8e34b33beb75760dfcfb7dde69d49a74c9ba99e9db241d2f8972`

```dockerfile
```

-	Layers:
	-	`sha256:d9efb313d20d5a25cf9f10e00ec84665331ad1e003399c0fef4844abeaa1a350`  
		Last Modified: Thu, 02 Oct 2025 06:49:16 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7-jammy`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68-jammy`

```console
$ docker pull clickhouse@sha256:2455198591401065314ff2379d501b6543ae2d23d0154ecce3987682105d0f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ee532f93a67d0ebe1b5f7facd78ae4924d4d83e8449e19563e5890612800c28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221872995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace943a6bad852154e42d7d55e184e1e323a90f5d400998204a73812b8f0dec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338961181e28194c64c6c93c82c6e1b5c507498d03cd17f0cec712d1fe269581`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 7.6 MB (7598367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2b25f06db7dd5ef076c44bb93b2e3fc9c0b7214bdf508fb05c2175493a8c3`  
		Last Modified: Thu, 02 Oct 2025 05:15:56 GMT  
		Size: 183.9 MB (183867787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40b10854508535b0877b307e1b086227c60cf63999693f91f066095e01874e`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9f6f588117ceae2f7c0ca5f2628779b06f3cfa69cbe4d4c86e53e8ad3b7c1`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a128886bdf0022c43525a955684f2ea66f896ae61215ff01c9ca0c351c48977f`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c6c6e44f6a69557bec3bbc89211a9b389829adad99a0f7227d000365e97445`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c6ae18b568dbb11563f1a63a5c87067d42772f40b8dc39b4992bedfe981ae`  
		Last Modified: Thu, 02 Oct 2025 04:54:22 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4bd221e686f8ded9b7cfb7661974666a3a109aae164ef281716761608092c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5cba0949b12e32f3c9417892a3dae9a6e9c0e89de66b6033864cf10cc849b0`

```dockerfile
```

-	Layers:
	-	`sha256:843aa375c11db0a50dc5c8883507e24e7de8123bf20762851a225278a6b9fa90`  
		Last Modified: Thu, 02 Oct 2025 06:49:47 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.8`

**does not exist** (yet?)

## `clickhouse:25.8.8-jammy`

**does not exist** (yet?)

## `clickhouse:25.8.8.26`

**does not exist** (yet?)

## `clickhouse:25.8.8.26-jammy`

**does not exist** (yet?)

## `clickhouse:25.9`

**does not exist** (yet?)

## `clickhouse:25.9-jammy`

**does not exist** (yet?)

## `clickhouse:25.9.2`

**does not exist** (yet?)

## `clickhouse:25.9.2-jammy`

**does not exist** (yet?)

## `clickhouse:25.9.2.1`

**does not exist** (yet?)

## `clickhouse:25.9.2.1-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:6a9b294926f6c788b4987a3135d20db927c1024b6fbe5031aebe63986501e8ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b49b8349d69eee8d52198e0ca421fbb4fb4eae674d3186b4a78fd9b447c1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfcd02381324b377d28f8d9ec8a98d79b247d4f7acd5755f200377d955260fe`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3087d2bec400b9007505dbe31af18228f8efd8f636b62742afd6d6e7769cb`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6bd958d4fdcf73d413a0bbd45417bbb0f9f5c18ad53ce40474e09d6b600df4`  
		Last Modified: Thu, 02 Oct 2025 06:50:18 GMT  
		Size: 189.8 MB (189754400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2463d540d48c402f1f1b00acd196d81fcb9b0bc0be1c70f4d1581b36db7781`  
		Last Modified: Thu, 02 Oct 2025 05:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715458a71adbefbb543edb05b4b62586937e76ec094624a7a4b015900e776b7b`  
		Last Modified: Thu, 02 Oct 2025 05:24:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9428e67b58e6c81efa2d16d20fa84c94d6ac637433787219aa1b67c54409d907`  
		Last Modified: Thu, 02 Oct 2025 05:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f66649922d640be9d60c3b9711edab7d6157e012c2efddec5990ec65946002`  
		Last Modified: Thu, 02 Oct 2025 05:24:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf02920bdd0d3731582afe82d2177fe3aecf91b64f8ad632f23b63526aa2032`  
		Last Modified: Thu, 02 Oct 2025 05:24:52 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:377c1cbe5d5c7d7f693fa79ab595b893890ecf5f28f14207513e462dc85c7eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ab94808279f69f7268d1425f8a374d81f62ea64745a524b49f909254aa9cf`

```dockerfile
```

-	Layers:
	-	`sha256:d6d30a62324496257fc1023c0c709423ffde3cdae9f95a05a3225db78d9b52ad`  
		Last Modified: Thu, 02 Oct 2025 06:50:02 GMT  
		Size: 26.7 KB (26670 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json
