<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.7`](#clickhouse2537)
-	[`clickhouse:25.3.7-jammy`](#clickhouse2537-jammy)
-	[`clickhouse:25.3.7.194`](#clickhouse2537194)
-	[`clickhouse:25.3.7.194-jammy`](#clickhouse2537194-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.8`](#clickhouse2578)
-	[`clickhouse:25.7.8-jammy`](#clickhouse2578-jammy)
-	[`clickhouse:25.7.8.71`](#clickhouse257871)
-	[`clickhouse:25.7.8.71-jammy`](#clickhouse257871-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.10`](#clickhouse25810)
-	[`clickhouse:25.8.10-jammy`](#clickhouse25810-jammy)
-	[`clickhouse:25.8.10.7`](#clickhouse258107)
-	[`clickhouse:25.8.10.7-jammy`](#clickhouse258107-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.3`](#clickhouse2593)
-	[`clickhouse:25.9.3-jammy`](#clickhouse2593-jammy)
-	[`clickhouse:25.9.3.48`](#clickhouse259348)
-	[`clickhouse:25.9.3.48-jammy`](#clickhouse259348-jammy)
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

## `clickhouse:25.3.7`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.7-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.7.194`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3.7.194-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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

## `clickhouse:25.7.8`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.7.8-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.7.8.71`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.7.8.71-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10.7`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10.7-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9` - linux; amd64

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

### `clickhouse:25.9` - unknown; unknown

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

### `clickhouse:25.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9-jammy` - linux; amd64

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

### `clickhouse:25.9-jammy` - unknown; unknown

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

### `clickhouse:25.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.3`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.3` - linux; amd64

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

### `clickhouse:25.9.3` - unknown; unknown

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

### `clickhouse:25.9.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.3-jammy`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.3-jammy` - linux; amd64

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

### `clickhouse:25.9.3-jammy` - unknown; unknown

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

### `clickhouse:25.9.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.3.48`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.3.48` - linux; amd64

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

### `clickhouse:25.9.3.48` - unknown; unknown

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

### `clickhouse:25.9.3.48` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.3.48` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.3.48-jammy`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.3.48-jammy` - linux; amd64

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

### `clickhouse:25.9.3.48-jammy` - unknown; unknown

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

### `clickhouse:25.9.3.48-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.3.48-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
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
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:bde1003bdd7930d9d68657379a4b5ee46416bb3abe5be166ace60792f13512f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

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

### `clickhouse:latest` - unknown; unknown

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

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ce5cdd1c68c33d6bbf14367959366acbe71ccd77ad3fe0aa5da8d0a8175d6364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214111119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9dfd2afd758df2ff51dc7a1945a597bc8acd1c130f8b0919885b5faed809d5`
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ed75ef53cfd6a9cfce0b561c36d5769b84d6f16cf038493334a719d466d2`  
		Last Modified: Thu, 09 Oct 2025 18:02:05 GMT  
		Size: 7.6 MB (7576686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362ea39e7412ed539646c725d50d856db476363ab6c707b6d5645af60041e59`  
		Last Modified: Thu, 09 Oct 2025 18:50:06 GMT  
		Size: 178.3 MB (178281305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317d08241171fe3ebb8c692fda28f8a1134be62baf485e6ac9379116a45acfff`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ceea9859933e28f108d3b4be556557221cd92dd5d2e27ee8f5cbb32a9197f`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb98e0443a1a92f5026bf6dbdd53771cd5846bf51b7fca42e24f5d7a55da7c`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118191d4c3575b6be10ce07ad4486f8ab3cef832f7a06cd61181ddff9a50125`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aaed5867dd2ba05d70381db24ab5425cdd03e2cad9082ec6010b09534fb92b`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e7ea58fb9f0b60d16fce2f49766b4f415ed80bca847a4f65e443341fa22c742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b40f33f9a4b9fbade572abb9584618989146c262f42d6024eaca15bc91318d`

```dockerfile
```

-	Layers:
	-	`sha256:b9268e0d33dfa09a8f0081d21988599d358299326f925e197732d806c2e092cc`  
		Last Modified: Thu, 09 Oct 2025 18:49:52 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
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
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json
