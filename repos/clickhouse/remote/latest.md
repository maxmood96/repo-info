## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:d72c1e22e8dd942150d7a295102ae1d054d89458c755fa384805c2b9d0ce906a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:b5e794a61dee6c9814d615dbc87e45df048ea8d7dc20ef71872987fb914bc3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212135268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe80ed3415270643a7f53e9832abf5e31fd83f432789a34e247fe4489709206`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2326ed4ccaf84bee60fa91f1042a05ee14314f0201b7fe31bc90f5486c0d8e`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 7.2 MB (7151641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39de22e59dd3bc8dc103580e3de98eed432a9812fab170d14db3f6b805ca581`  
		Last Modified: Thu, 10 Jul 2025 21:50:02 GMT  
		Size: 174.6 MB (174577917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a47d602b72e072a852f6733815ad8d2ff3a07734a242da8ee574b55374df7`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb821ab3667e6c511d025168a0f2156b1de05d4379d6157d03e45ffd169b8dd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687359a621bd7634c2e21c8fed6ec70f58901ea16dbb06d14def470a34353fd`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc585dcea2120548c77583fa407795aab7e9a6e35d86e54be33d9cc044d4fc`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0413c0d5b1a3dbd82cf5553129e964b133eeb4fecb5ab15c358f6d436ee643`  
		Last Modified: Thu, 10 Jul 2025 19:57:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dba8946c069b8df2b9f6dea0c925339e4a4b79b47d1d4f0ae254b66c5dac7356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7896194fbd126883adf07d6a89ae86ac9a7ea70ee1b7f0c6bf6bc184851c9`

```dockerfile
```

-	Layers:
	-	`sha256:9202ad73897a10f13a28696968be4747ba1f794e0f98f59052e9f7f176d1c8dd`  
		Last Modified: Thu, 10 Jul 2025 21:49:38 GMT  
		Size: 25.9 KB (25884 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c974e82b45e39b519a96c7a320a85b170c4db5168c3a2cf7936ed64dbb68c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198272745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271535d02c86e66bc261b371f122629085e9f92d8974f537d5bd2af065af349d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 16:05:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 10 Jul 2025 16:05:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPO_CHANNEL=stable
# Thu, 10 Jul 2025 16:05:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 10 Jul 2025 16:05:55 GMT
ARG VERSION=25.6.3.116
# Thu, 10 Jul 2025 16:05:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 16:05:55 GMT
ENV TZ=UTC
# Thu, 10 Jul 2025 16:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.3.116 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 10 Jul 2025 16:05:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 10 Jul 2025 16:05:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 10 Jul 2025 16:05:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 10 Jul 2025 16:05:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bec5d5c045f33a4b1d38c3fd1f830388ff6b49fb70168c1f95c24fe851a03`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeafbaf1396cf9ab12cc685a070c0b26e4542cc7cde15612718416dc1a61fe`  
		Last Modified: Thu, 10 Jul 2025 21:49:57 GMT  
		Size: 162.9 MB (162915550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a557ea52735077adbf9bbeb6927caf304dcf4f078e2c68135a9c011fc6c68`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308223482e1d0ecce0a840da194218d759187721d2a588332c782ec761c49e49`  
		Last Modified: Thu, 10 Jul 2025 19:56:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ebfb747b675ef08a249559eceff45e4352fd8350d93e672272d95bc2c3759`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e39bcbaf0db63da1517b2b6378bde45337da1fa3f1fa9a520ee0dbc7bee38`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f558def534ac3e37c01e09ab5564562743046479c172936eb6c776b3a23fa`  
		Last Modified: Thu, 10 Jul 2025 19:56:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bb157beafb37aab747bfc58b3c2d3847c0405836114d34213de857a899a2be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7c710b5f9a6ed59bf5bd14c696faca3ba508df6fea4bf2829dfc210b542bb`

```dockerfile
```

-	Layers:
	-	`sha256:0322f9bd2f8bf8755392c1bbcb9cbf756ac3eb4c28fa3d6971040d4f6e3a1e1d`  
		Last Modified: Thu, 10 Jul 2025 21:49:41 GMT  
		Size: 26.1 KB (26096 bytes)  
		MIME: application/vnd.in-toto+json
