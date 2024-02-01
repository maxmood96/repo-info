## `nginx:1-bookworm`

```console
$ docker pull nginx@sha256:985224176778a8939b3869d3b9b9624ea9b3fe4eb1e9002c5f444d99ef034a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:1-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:161ef4b1bf7effb350a2a9625cb2b59f69d54ec6059a8a155a1438d0439c593c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70503731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8758716bb6aa4d90071160d27028fe4eaee7ce8166221a97d30440c8eac2be6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7dd3ed1dc34cc1caba38bbbf22bceda5bd2e7c4e1b3c11ca64cda2ed186a2c`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 41.4 MB (41373256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35497dd96569b9139cd388fd7107df32ccdc1449b205536bce0968b2dec3e7dc`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36664b6ce66b304efa7ba48eb960133a085c2ec800a9f8887df94a82679334c1`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d455521f76cee8b8b2e21457075cc500c60373d70acb217f12838818fc3da90`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9c4fdb83d69ef5986ec344c6b75606b3a417c7434268cb6995962be5312f14`  
		Last Modified: Fri, 12 Jan 2024 00:22:07 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056d2bcf3b682573ee5b0c176c1209df285d5be0df98ec6ae08bf7421179b74`  
		Last Modified: Fri, 12 Jan 2024 00:22:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f7c78e8bb18ac2866523fad6d4badba983a56527235f79480638e4fbbac924c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e31210b1ac40c98f7c5090ecfa6fb451c94fab9f3779f0cc5173b77cbd0a9b6`

```dockerfile
```

-	Layers:
	-	`sha256:10a72dc35ed3bf41196a272672d097d612d42a8d7d81522fd137fb527d209189`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 2.6 MB (2552271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ce4daf9edf7e4dcd071011d083e05234c5173137f8dbf98d4c32fd31260ffe3`  
		Last Modified: Fri, 12 Jan 2024 00:22:06 GMT  
		Size: 30.2 KB (30225 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:02a7b9210d563862c699724d7d56bc70bd176ee7779faf0c4d6884db11880b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63075897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cd35587a96339c75c9471f3fecb6b42d512cd90132e2dc080dae3206241e4a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e847691f46d05cde8122cce13c292eede59e90cac1b5e17dca0f2976a712068b`  
		Last Modified: Fri, 12 Jan 2024 15:45:17 GMT  
		Size: 36.2 MB (36185853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda011b47a12a4fc48c763ee99c980d4bdbabbbb269f38bdcd3292c1ef833679`  
		Last Modified: Fri, 12 Jan 2024 15:45:15 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe74211f3f7af4f3cff85e1fe810f143655d451d36d15d843a11af98c8095bc`  
		Last Modified: Fri, 12 Jan 2024 15:45:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65906a1fde4dc637e1c6cc8b27707ec88bbafe0b6bbadc17d2d42b814529df`  
		Last Modified: Fri, 12 Jan 2024 15:45:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d898a47a71f458da5ab8e210e89d0fcf1716ec7bd99b92dee04cf21a53d43be`  
		Last Modified: Fri, 12 Jan 2024 15:45:16 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc9333b185fe72561ed40c7c2a05a972972ce060088143a7402b1f2602258b7`  
		Last Modified: Fri, 12 Jan 2024 15:45:16 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:1e14315a74adbf19ff8d900cfda97b8a8f6cb4475c7722ad68bfda3cabbe845c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a54da476b0235dabb7434a05b68ec16a55f61441e43cea967f389df9f3bf8`

```dockerfile
```

-	Layers:
	-	`sha256:15ecf2f32db751b93f87c49d21e5a874de75feafeacd77df7ff1165b5ca05f51`  
		Last Modified: Fri, 12 Jan 2024 15:45:16 GMT  
		Size: 2.6 MB (2570730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca3abff14c18c76b13ddd838f062c36407e3208d3f5e6a9cf934928326293d6`  
		Last Modified: Fri, 12 Jan 2024 15:45:15 GMT  
		Size: 30.2 KB (30176 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:563b62837fcc7890d81d8137688b0447181f782de8121acf16d28a792a35dbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59460317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26daf664e62fe9fc7d7dc8c549d9601c0773be47cdb3ec13e9000db5d61e477f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27dda94a38816ccb19eb832992967d720ebcf3a2142a3096ddde3c10e2d65b3`  
		Last Modified: Fri, 12 Jan 2024 19:12:20 GMT  
		Size: 34.7 MB (34737626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c44f75ca82881a099236918e653cb144ddfa05f1333160b15b6252ce372a97`  
		Last Modified: Fri, 12 Jan 2024 19:12:19 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ffc8323e3934aa1dbab569d464ff5ba1f7bd05cf35c1f682e3b90c278167b`  
		Last Modified: Fri, 12 Jan 2024 19:12:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ad1bd2c341543deb592c075c509dfc9397ea914a2edc9accde852aad1506f`  
		Last Modified: Fri, 12 Jan 2024 19:12:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231b72a4ca7148885d5a84809b7feb9e8c822e55bdb4d2aec7c745accfbcdcc`  
		Last Modified: Fri, 12 Jan 2024 19:12:20 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f88f1f94fb6d3d1bf758d0ef209361f59a3c394f034a05474c7c8c40045f8b5`  
		Last Modified: Fri, 12 Jan 2024 19:12:20 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:bae07bb6dc6508fe1fa336548cc3cf2daff479f2d4abfec57f3fb3e091c8777e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b3686151bf060225999fc7c3179acec9240ed1b3df27b96d0aca523c589270`

```dockerfile
```

-	Layers:
	-	`sha256:5cb18c719dcf0c60e0fcfed7c0df9e4a004fd6c726f014dd6df9b4f87201460d`  
		Last Modified: Fri, 12 Jan 2024 19:12:19 GMT  
		Size: 2.6 MB (2570052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a74552645a034b72fe316787f0b090ce0dc5d785a9aa406e99b05f9f738df40`  
		Last Modified: Fri, 12 Jan 2024 19:12:18 GMT  
		Size: 30.2 KB (30176 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:523c417937604bc107d799e5cad1ae2ca8a9fd46306634fa2c547dc6220ec17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67202480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7be49d2a11cfab9a87362ad27d447b45931e43dfa6919a8e1398ec09c1e353`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8897d65c841707a2f02937de91c6644ba9699bd3ad194bdd84d2b61a93ca12f2`  
		Last Modified: Fri, 12 Jan 2024 09:19:06 GMT  
		Size: 38.0 MB (38040594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc138d1d206d59261b82b2c537e7819ca8f46c63ce80b4906394a8b83ea896a`  
		Last Modified: Fri, 12 Jan 2024 09:19:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f386eb918297ce19936107ccb010187b2d6a95ba8bd60073610d371289b46c`  
		Last Modified: Fri, 12 Jan 2024 09:19:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb2f3db77c35ab11eccb3643b18e72e1085fcc42343078da8d72b76a6fd5b44`  
		Last Modified: Fri, 12 Jan 2024 09:19:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fb762834ec1a0ca5d5980d4f810342d9fe5f1cf96b4d4bf2d4a27a564778ca`  
		Last Modified: Fri, 12 Jan 2024 09:19:06 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a7e61f6ff45ab19ba3bad8bfc4e38cdafbbca0cefcf1f81516bb14b6476557`  
		Last Modified: Fri, 12 Jan 2024 09:19:06 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:3bd66d9f2dde2fef40a4e8957a06fb42976137eb337e7496cdc3957220ca2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0e6682270023bb2b097f2fa0ebbf2e4193073d957cfa9cdc5b81fed703927`

```dockerfile
```

-	Layers:
	-	`sha256:b5c71c53363f4930c0c81a63d5e5e4aa4681e7f3c9b5f24771065f4aef5dbe24`  
		Last Modified: Fri, 12 Jan 2024 09:19:05 GMT  
		Size: 2.6 MB (2552722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a977dec78ebd58b02ad596d5b14c68ace7c3989c944a63ea601082399ff215b`  
		Last Modified: Fri, 12 Jan 2024 09:19:05 GMT  
		Size: 30.1 KB (30079 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:0b0c1d0dcc3c634fa51981b5d439dc4ddf76ba220407089e9709f49ea7d228ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68695362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853bcf78fbb382af6c6a4428e7556798a8219b95c16ed98e2532effec962c1a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aaeb00755a525c33532559abf81c2aa41af5abffab07a66d9b006c8fe54b54`  
		Last Modified: Wed, 31 Jan 2024 23:58:43 GMT  
		Size: 38.5 MB (38525777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc21db4e81318d23bc1da6bdab57cb7ce5b12a3260adc65aa0284cab272c1d45`  
		Last Modified: Wed, 31 Jan 2024 23:58:42 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b554bbe9a5dbf8edffefe09b807f3b89facddeac6acb3ebc4aa57282b3dcd0c6`  
		Last Modified: Wed, 31 Jan 2024 23:58:42 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedf340f2af413bed66a7453f9783b52d65277215ff7e0d414e54a96619c186a`  
		Last Modified: Wed, 31 Jan 2024 23:58:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43e170b569169c7f3ce4a970470dc5cd003963f60dc35d299b6bfb3038e56ab`  
		Last Modified: Wed, 31 Jan 2024 23:58:43 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502dc342d77be3ca034b47a5809fc2495c3025cd99c4b6c5c0fa6ea1b99311dd`  
		Last Modified: Wed, 31 Jan 2024 23:58:43 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:98a1512e032a3097883a4e43d3773968ad2514d86eebf8b1f74fe7eb138906e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826795826513385b5ce3e8726d848122cdc625acc8c2757fd0e22e3017734d97`

```dockerfile
```

-	Layers:
	-	`sha256:2ad93c21cbeea3056e0281fc61fc13d2d145cdcb565ded26a31d1fd82bd21e8c`  
		Last Modified: Wed, 31 Jan 2024 23:58:42 GMT  
		Size: 2.6 MB (2563209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6535103f5fc4cb39b7204bff305b1c1e2016d38017b3e831e5c6a20559833a4f`  
		Last Modified: Wed, 31 Jan 2024 23:58:42 GMT  
		Size: 30.2 KB (30166 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:12bf3d3dbf975889456ed1a184719f06d65af51e2a6673c3f38b9450e086cc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66174859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e9fb500f9f82962c698be271d0852fdd5bb20c78d99d3db3237c88045fb691`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123b7b041642fd48a65188f89d8a1ac8dc9115419b73632e6c6aaccf3073691`  
		Last Modified: Fri, 12 Jan 2024 04:18:54 GMT  
		Size: 37.0 MB (37048897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2dc709ca4c1de5a54a8c6587213f7de47c2d5678f642591b8f1f2bbff9dba`  
		Last Modified: Fri, 12 Jan 2024 04:18:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7687c87b05f212e63b1344d36fa915d509897ac7be47de7867bd48891a02b62`  
		Last Modified: Fri, 12 Jan 2024 04:18:50 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb3e416592bce06d1cc650c0a5c08d5e7d02f1d8e3891a5bb1557d3d5ffcb97`  
		Last Modified: Fri, 12 Jan 2024 04:18:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e055a2682f4a3899af2e2f49da301754b3534d5e80499358a4073d69397c554`  
		Last Modified: Fri, 12 Jan 2024 04:18:51 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b78c3eb9fd4011622e27f4c8b1953ead2c91d3127d15efb38e4fff80846214d`  
		Last Modified: Fri, 12 Jan 2024 04:18:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:35a707bebd92e639a71fec1d5b344a4eb00f113123e38c54a5b84962928f5d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 KB (29954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeba4a9ce0365a8583cd397dcf687151976d3f5649af18a9d557340881ba734`

```dockerfile
```

-	Layers:
	-	`sha256:f240738a2112072c68bee74bbebb78259b42bdf846b9d9e367e304f2107adde6`  
		Last Modified: Fri, 12 Jan 2024 04:18:50 GMT  
		Size: 30.0 KB (29954 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:74d855a67e65f1160751618d192f4f5e87e24bf89edc5252c72cf1dbf34acc2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74920753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cfde8fdbcc4b4e0a04f1fe12cb38de7536197ca11b7f3e3bc5a6b0cbce2ba9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2415a9d9f2761256de8fb8099ae09b74edf42aa7195b62aa52b7c5bb9c20f1e1`  
		Last Modified: Fri, 12 Jan 2024 09:29:34 GMT  
		Size: 41.8 MB (41795663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba815cc62526ea16c17d0a2fd8d26eafda2be5369fafb645734cdb4ea9a8f4c`  
		Last Modified: Fri, 12 Jan 2024 09:29:32 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd29b7b9d3ae517d62150a49e74137124427d324a8e358e223ac711c09cfb579`  
		Last Modified: Fri, 12 Jan 2024 09:29:32 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c811e7d118c3ddf78e0953a67a1cc182f0ac498f6c77a17414c459b8bc6bf`  
		Last Modified: Fri, 12 Jan 2024 09:29:32 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0c1fa4baf53fcb8c2d4cf467cf55eeaf3b6d7c2ce7f640de3079cf781be9ef`  
		Last Modified: Fri, 12 Jan 2024 09:29:33 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6a10c2c839c9451c48419c58add2cc504072cd65b93d9a0874e40788a713c`  
		Last Modified: Fri, 12 Jan 2024 09:29:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:5f16a3e962a9efddac4427abcc5a0cea86cf2a4c955464ea359355ad110df89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6605ae9e464fdf9bcce7c92c6f492996e09fed8c595a4f4b0ffbcb62d40afed4`

```dockerfile
```

-	Layers:
	-	`sha256:f032bd4d1a70ba4c5334f0ad079cfdba973b357af7bd7768d6a9607e23f05672`  
		Last Modified: Fri, 12 Jan 2024 09:29:33 GMT  
		Size: 2.6 MB (2577086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0537192edc68735fad149ec82a0a7c15c18df0585f92c61ad2f465f9f7a038c8`  
		Last Modified: Fri, 12 Jan 2024 09:29:32 GMT  
		Size: 30.1 KB (30132 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:89e972e7eb90942f2eca90997a93cef00e3b2be03f6bd85c31e8c976950b9d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64821371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45aceeb653832397f4536b54b7941f18abef9c8249e9a1649cd1379f4ea7a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Oct 2023 22:44:45 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 22:44:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NGINX_VERSION=1.25.3
# Tue, 24 Oct 2023 22:44:45 GMT
ENV NJS_VERSION=0.8.2
# Tue, 24 Oct 2023 22:44:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Oct 2023 22:44:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/usr/share/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Oct 2023 22:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Oct 2023 22:44:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Oct 2023 22:44:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Oct 2023 22:44:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629e01b46d0a79485d2d2c349295b272861401d89a05973ed3905682ee98d132`  
		Last Modified: Fri, 12 Jan 2024 10:27:12 GMT  
		Size: 37.3 MB (37324963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b89fc4e341c886c213c681a4c4369832eb945d954b5752dd92a0daff7ecf41`  
		Last Modified: Fri, 12 Jan 2024 10:27:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44779fc292167b606c904f93668e2c74fcb45ca6d629b791f2c243af6f47e05`  
		Last Modified: Fri, 12 Jan 2024 10:27:10 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb1d253871c577ee56e34cdaa390fe8bb2d8d993d73b2654411086a87a3a2f`  
		Last Modified: Fri, 12 Jan 2024 10:27:11 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347261cc8c6e1b121af72d344f1828f8a8d88af1ac8aee65cc621286efd026`  
		Last Modified: Fri, 12 Jan 2024 10:27:11 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbde22fd16a0d881afd364c406aab491928c3f31fbd2909204f05be668ddad5`  
		Last Modified: Fri, 12 Jan 2024 10:27:11 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:11d5be60c7ec8c56b3669a2c000bc304f0ce145b3c6d28423334c0bf52683bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82083b7fecf1b53c06efbf0f9e7b2faba0aabd3ff8eee860a4df2e5b8c3a0cee`

```dockerfile
```

-	Layers:
	-	`sha256:a62b7fa58a8d2507c7d80e09d366e77436f97fda5b5e968312c9026dc8349936`  
		Last Modified: Fri, 12 Jan 2024 10:27:11 GMT  
		Size: 2.6 MB (2561670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19935c5fd384b547ec94b910bcfb5eea028e9e7d1199da7f25411da2ef9d1ecc`  
		Last Modified: Fri, 12 Jan 2024 10:27:10 GMT  
		Size: 30.1 KB (30058 bytes)  
		MIME: application/vnd.in-toto+json
