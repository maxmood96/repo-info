## `nginx:stable-otel`

```console
$ docker pull nginx@sha256:55d5034fbfe4f25f8ee55d70b5d723bf08a562e2e8d1da0ae4b5d6b2d69ce0b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:stable-otel` - linux; amd64

```console
$ docker pull nginx@sha256:1a28292547663a7de6dec6f779c138825840a0bf05c28bb3d57f6577ab338cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73953798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704632a6776d744460f98dae66660b4706baacc27662acca9dcb12ede8953b2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 23 Apr 2024 22:15:45 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 22:15:45 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff9273d4bcfbd6c1fb9ad5d803277084d29ca40b01228ade1c885dd84a34c66`  
		Last Modified: Wed, 24 Apr 2024 04:55:39 GMT  
		Size: 41.8 MB (41817059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7711b9f4e54f8190b75ed1442c8be3ef10aa76edb21f5d24ae83434812f9eb`  
		Last Modified: Wed, 24 Apr 2024 04:55:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24226f3ffcd577ea534ae674a6e81d5c4ed546c75ef0a96c8a0b540b32d99e79`  
		Last Modified: Wed, 24 Apr 2024 04:55:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a20825229654cebfd21829a552f7288e85ba5c33e58335f642746bf70e412b0`  
		Last Modified: Wed, 24 Apr 2024 04:55:37 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb0f54d68cc1a9be8b19211147257af72e1d8cec0fd68e802901c119de46a0a`  
		Last Modified: Wed, 24 Apr 2024 04:55:37 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2685e6fc63991216aef6c7115230db9cab81a8457cf7f641e12b0fedce0a7b4a`  
		Last Modified: Wed, 24 Apr 2024 04:55:38 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5a692375f54ca72ae5c5e01fe5aaa4688420bec5fb2053e3d5926d25e706c4`  
		Last Modified: Wed, 24 Apr 2024 05:58:05 GMT  
		Size: 3.0 MB (2981679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:bc5448c7de5dca0679bb2974300ec64e6704df4893e5b5727528a8a3d9ea539b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b377659ecfa153fb475bb8f265a763f390140e4c15e679fcbe424091285dbcbc`

```dockerfile
```

-	Layers:
	-	`sha256:b818279b55e378e48d7bd1823be38adf200ff1dde9dc401c68614c9dcc8cc03c`  
		Last Modified: Wed, 24 Apr 2024 05:58:05 GMT  
		Size: 2.9 MB (2916186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0a45424475340c6111c86d7200df39825acdf3b5eec326fa0505d96bcf5fe3`  
		Last Modified: Wed, 24 Apr 2024 05:58:05 GMT  
		Size: 20.6 KB (20634 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f8e4a2ff49c0763649d3ebf5973bd5dcb851e7ab2f0610353d9e5a0e0d6c83cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70471340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd92e34c75aad6c58f6ff29ad7215b5b2877fab36a6ef4e5bcaeec67b93d93a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 22:15:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 22:15:45 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 22:15:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 22:15:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 22:15:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 22:15:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 22:15:45 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 23 Apr 2024 22:15:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b13993b7fee0bee4795b8e52ac9e5cf3e6bc923bb9ba737dca5be336bb535`  
		Last Modified: Wed, 24 Apr 2024 02:22:42 GMT  
		Size: 38.5 MB (38459490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6510588b5777412d74f80b6e628d7bb094bcb737a162113368dc0db888318a34`  
		Last Modified: Wed, 24 Apr 2024 02:22:40 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1033b5584233874819a86fa0506cd7dd6d902d36e97c39ee1bdec212cb0fa97f`  
		Last Modified: Wed, 24 Apr 2024 02:22:41 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa1a1d16d442fa1261f40573e8753cdc0e66d55bbb41770f9aeac31672919a1`  
		Last Modified: Wed, 24 Apr 2024 02:22:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c723cf493b850ecb94694f6ae4f63d4358d40263ea17351a44d6b0f8393db7`  
		Last Modified: Wed, 24 Apr 2024 02:22:41 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d17d1103ca421d1f189726552b35e3fed282de689abdb3d31b85f2a5821f1`  
		Last Modified: Wed, 24 Apr 2024 02:22:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7879fa78e906930827ccc50a54ddb7a31837dd5180a12fbb56ab662275578dca`  
		Last Modified: Wed, 24 Apr 2024 03:15:32 GMT  
		Size: 2.8 MB (2845106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:b15a75586f072b1d9649f96a9a366e725ab966471de371fffe30329e3c631c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d85e499290607bda6e481a2fc6c26c4c1551579debc655555610c6d4b2876`

```dockerfile
```

-	Layers:
	-	`sha256:9826e74fc67b5855bff7ca59ecb8bc693da15e99db89950e934d2080b49f3198`  
		Last Modified: Wed, 24 Apr 2024 03:15:32 GMT  
		Size: 2.9 MB (2916524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ca24437e04eb1eb29a67722d1a503a7fbcd60a3f47a00945dc57d554f72a23`  
		Last Modified: Wed, 24 Apr 2024 03:15:31 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json
