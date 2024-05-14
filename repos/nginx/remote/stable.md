## `nginx:stable`

```console
$ docker pull nginx@sha256:f00e9a27310a9ea8205798d5dceca575a0c7da11a24a82e6ce69bc3f36317082
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

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:ca8ab6937d82742def7091d0655db0067dd30f38b5deacdc1bfe8702ced46bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70972103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d94e81d74c174995b4eed523339013e0d022f9f4d4ef54316fdad93142bb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13af041419fe58fef6eab2d929769a054b46d98b6d53b4af5eb60dde55ee0632`  
		Last Modified: Mon, 06 May 2024 17:58:03 GMT  
		Size: 41.8 MB (41817042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a2f02e459b7f1eb62c38b178f5623a68a3f04445778e9f79dc34f61cc0a49e`  
		Last Modified: Mon, 06 May 2024 17:58:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325ea416f2bb91b3a2d7b13101a3126bdd61010b3c1d39acbb5bda06774a9cb8`  
		Last Modified: Mon, 06 May 2024 17:58:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98760cd21ba689b7b54086720e2415be8e92a735c4714bc184eb05a2f12d6060`  
		Last Modified: Mon, 06 May 2024 17:58:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77702ab394084d473193d0929cadab39183b29731c371b021e280d065b4f60f1`  
		Last Modified: Mon, 06 May 2024 17:58:03 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d095688b3926a8727386c5c7e09abd56afbeb3cc7648adcf39c7c596f187c4d8`  
		Last Modified: Mon, 06 May 2024 17:58:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:43bf004e8bd63186e30970e5dbd22976986eca5b8dca72c62bf1f5a5535cd645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c907de7e5563aeb3635c675ac61c095245dbbef32aed1751c7de21244455db`

```dockerfile
```

-	Layers:
	-	`sha256:562b3b3daf615871f61d05eca9b5c44a209ba47fcea79385af4ad5edff259c0b`  
		Last Modified: Mon, 06 May 2024 17:58:02 GMT  
		Size: 2.9 MB (2907241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98848e102b16a1711a0f1c4fd77bd0b13f5f2746d856e5af6cadef40cb00b8da`  
		Last Modified: Mon, 06 May 2024 17:58:02 GMT  
		Size: 29.0 KB (29048 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:f5596acd2c96e284b6c6fefad9ac6e89f240e208f21da214cb074d6f8ecbe603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68154052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ca2ddeed45d6c24d92a3b0ea1786b56c7823f375727a994b2af2ed2be4679e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8438c8c0d12d9d002f8c76a323326a8707c21c91f52384dc79044482e723c7`  
		Last Modified: Mon, 06 May 2024 18:10:27 GMT  
		Size: 41.2 MB (41239431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6634eec8ccc87ffcb28c9d8a0b4e98419266f9693ce82e9d5041e8e011858b`  
		Last Modified: Mon, 06 May 2024 18:10:25 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87058b33a09d52953c365998796deaec8d0ad3ecb1ce6c66193391e53d0f459`  
		Last Modified: Mon, 06 May 2024 18:10:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9b229f3c52a684433d1752c46ee537cdafd9dec69642751feb58b384709aa7`  
		Last Modified: Mon, 06 May 2024 18:10:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7b3bcb22ff8c197d132cef790b746ad20d1db5821e6f646e4fba6075f3be1d`  
		Last Modified: Mon, 06 May 2024 18:10:27 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22405f8f0871dc1abeca6ce4ecfc112eb8fefad9181ff34985beaa3feafcb0dc`  
		Last Modified: Mon, 06 May 2024 18:10:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:1ded7af8abfb1fa588baea95d716897e60b92c10f7d66b601bd7e6c48d5987b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a141ff23989ea96f438200575116e81a0135cc295d107c671226e74bfe67c7b`

```dockerfile
```

-	Layers:
	-	`sha256:d19ed0e4499d6eb7cfbdaeef5ad7cf50f3ba549af56c1d8c0ac188fe7dc07949`  
		Last Modified: Mon, 06 May 2024 18:10:26 GMT  
		Size: 2.9 MB (2928014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c254992e4c334798122573264c244634dfce02f1fac0e6c707a64e3d754f4e2b`  
		Last Modified: Mon, 06 May 2024 18:10:25 GMT  
		Size: 29.0 KB (28967 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:e8dc5e74fad4c9756b0414dacf271abdc3f5c6fad12c090312ed12d82d43766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64207519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9567be5823d28a4a4fb8fe270665d55c5c766297646e2098e0b9966ecd4ad41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22651e96d46e8ac2a3592f36f7b38ca8cc46eb778b018e63707c010a8f0a93f`  
		Last Modified: Mon, 06 May 2024 18:55:40 GMT  
		Size: 39.5 MB (39462492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f75aca463dcd2ce3dd37a6cb946cdff4f4ce5e9653e9d15603169a52e3bef8`  
		Last Modified: Mon, 06 May 2024 18:55:39 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d238def1034fb203b20647cbdb6a813804c122cf1adaab6bfb66c17a3f868b`  
		Last Modified: Mon, 06 May 2024 18:55:38 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75892764031f465d7ccb2ba1c830b4b3bf2986c54d2b78d54a6348c82dc29f`  
		Last Modified: Mon, 06 May 2024 18:55:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4590c1ebf3eb1c2ff63178c5717ccb3a565d77b92e490b6595d47d7fb3fecc`  
		Last Modified: Mon, 06 May 2024 18:55:39 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fc840a6d2652154329d4e092b76e487acf0dfb35731a8c66ad1582decc5c1a`  
		Last Modified: Mon, 06 May 2024 18:55:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:527d537b058b04350fd811b368ff59bf29f5294a7c4609291c320d1e708472a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b90c87d287d5a8450fcc46d2643013f14695576316a9391ded8d82d23f3483`

```dockerfile
```

-	Layers:
	-	`sha256:f869b569f2da6768b4bbb95efc7e99afdd225d6e9168715bf500f024a7fced76`  
		Last Modified: Mon, 06 May 2024 18:55:39 GMT  
		Size: 2.9 MB (2927230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444b68dacb98f205a713723f59b2981b2be648b9e032c20e0ccad2605b19d461`  
		Last Modified: Mon, 06 May 2024 18:55:39 GMT  
		Size: 29.0 KB (28967 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:e5ff12d60be2833988d5b2a77e835a8b6342f5e625d89f0bbdb459e6a8dd11e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67648748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765435e93ffa66a35e47761ae8b31bcdf92dc2cbf311493196f1b8e9849b4dbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d863eb53c9c52c0b1d013a7779f6d25371ce4c11a0a1fae408d0c11529854d5c`  
		Last Modified: Mon, 06 May 2024 21:13:57 GMT  
		Size: 38.5 MB (38464222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d9c807044cd969a400ad4db223bd2efc3f0b9a36856a42cdb21ee40432ca64`  
		Last Modified: Mon, 06 May 2024 21:13:55 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfcda1e9458d1e1f18d23ec90e3170ffcbefc34cbff5d6f18d8074286a96fe`  
		Last Modified: Mon, 06 May 2024 21:13:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550fda5d88cdf7516b4ed1c4835b299e816e1c80a3ad721b7314d7100a70d704`  
		Last Modified: Mon, 06 May 2024 21:13:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839784a1f9ab26cc9d0cdb9ff1c8c2e7f953051e7167fe3ea1ee4e851419faee`  
		Last Modified: Mon, 06 May 2024 21:13:56 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4228b37182dfdf55e28e483d683a7de8da8c3679ff54d6f52debf4e51fe978e0`  
		Last Modified: Mon, 06 May 2024 21:13:56 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:4fa51343ae618646491211d820bd7e6b77d1be181ff1ace128ffd641716f8328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e0cff133e1496d88b30bc99c04f9c4d8f497f0e717f86c826925382b8914b`

```dockerfile
```

-	Layers:
	-	`sha256:51d465aeb71fe3a475fb0708c6ca524be22c9e953bd4e695208c8f00821e1df5`  
		Last Modified: Mon, 06 May 2024 21:13:55 GMT  
		Size: 2.9 MB (2907578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40337e01dcf44a9e9eb2ca02c78945c23a338bdd86cae3fdf87923aeef5a0d7`  
		Last Modified: Mon, 06 May 2024 21:13:55 GMT  
		Size: 28.9 KB (28895 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:245e280669961195db555d4d8224479d8f439a47889e72e7ab0f198cbfb1170f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69136017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b4bc9bfd522e33a771172df9544747f8cd321e2349abf695d4f13ea4340ecc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 03 May 2024 19:49:21 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Fri, 03 May 2024 19:49:21 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dc47c0070e33e744e61231a608c73406a213d736b18855ad801c3e3be0f9`  
		Last Modified: Tue, 14 May 2024 01:58:47 GMT  
		Size: 39.0 MB (38968798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c14d54de70d4a44a1a8e826d341c382875ca129c5615237776b33f507f385`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6884753b649552fb035b3af87e82a51925540bd1643832727e377a7d66753f`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b41cea127fb0e254525acb65129f42bcf5efcd2f94fe368e5728efaa827a9b`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f733d0f99b4fc939061da4200b75be632d93eab5f4c9c9e7393a4adc3e93e9ed`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da38658c88e5b8326c8c6d2ef8b10b50b20673bdebe3a41a7a72c0199faa1baa`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:871395fd9f76bfe3aac972bb2d79cc3c5b2fbace8d315e494a9243731d637080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2949480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9d7b8b829729963e25522845b8421e75ddcd3663c6cffd5cfc43168054aef6`

```dockerfile
```

-	Layers:
	-	`sha256:156f1a04f6d0d0de8421988c74401df495a54c76b331270532a3915acac7a17b`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 2.9 MB (2920471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b06b1c7e919210704e21020dea8592d442fae2c0a042e3e6bd88d7a7a112267`  
		Last Modified: Tue, 14 May 2024 01:58:45 GMT  
		Size: 29.0 KB (29009 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:5c688254507ac6ef1c3e5ebc8bf1b7719f1e9cf91579427129be970b51948dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72511635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20c3f66cbbfcd9ca2eb72f2f4e2ad3e6260bd865228cda3e59f7d465cddf5ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8695717d7cf2ade3c00c7c67d34ae6a5400eb931dc2cdc192a7490881f6058d4`  
		Last Modified: Mon, 06 May 2024 21:04:02 GMT  
		Size: 43.4 MB (43362865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce61bae01648c9ccbefc9f10258423bd778772608139a224f0396aec6a8a0003`  
		Last Modified: Mon, 06 May 2024 21:03:57 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d864014d2c3d9ef74ce40b3389f1891a0eaebc76a7a0e49a346015403e1623`  
		Last Modified: Mon, 06 May 2024 21:03:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd77305db2ac5e5ceecaf5b30c9b11f03627d7dcc26cf80f09f9ca4439ef170`  
		Last Modified: Mon, 06 May 2024 21:03:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488a2381eb5a27366164d5411274c0efbab325c1d8cd159b170437f4050ce59`  
		Last Modified: Mon, 06 May 2024 21:03:58 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7689f07db4ba647729c9c58fb303fef74d2c2d8bc76a6873717e51764e19b0d`  
		Last Modified: Mon, 06 May 2024 21:03:58 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:98334caad163ebc459da9465998a2e1a91e72d38be803f42e4b11f0175d06475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 KB (28737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4613d94d9135ba4a72f481e75e02e128e1d30b8900e0449ff849dc33706b48`

```dockerfile
```

-	Layers:
	-	`sha256:8536a16f1f1b6cb2b2cc25ad934786a8995e44a6769997782aeacf9777159ebd`  
		Last Modified: Mon, 06 May 2024 21:03:57 GMT  
		Size: 28.7 KB (28737 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:2c343aa802866d622aa67e0b6584974b7a5495d6c266e1d580ea0fd0ae98a570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82063569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816f4040a2c48dd9ddf7be2690af749fd9c792b6414a2a644112cc7b08fc66e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055223d8b7ef640c6ead346a7b779415eba98a470445a7cc9df18dbe23321407`  
		Last Modified: Mon, 06 May 2024 18:27:53 GMT  
		Size: 48.9 MB (48917772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9c6971c8b879121f6a0d16268088562ae1508c595c6c49ea4ce9788ed0536d`  
		Last Modified: Mon, 06 May 2024 18:27:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42259a39ef62ef455b7dbd8f1105e6ca6ac95890e57dab7bfe6c86f7e404681`  
		Last Modified: Mon, 06 May 2024 18:27:51 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00d6914694a9658b90c5ff5c50482b5ce2535b989405b4d846b86449746109`  
		Last Modified: Mon, 06 May 2024 18:27:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb00c0a0e1266952aab1bac491d42f2578afc8f96a8db95cd02126e3cfb1a95b`  
		Last Modified: Mon, 06 May 2024 18:27:52 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56530b78cb617141e087d1038fa0f89c3f80d9c68043d3594dfdca9731d29efe`  
		Last Modified: Mon, 06 May 2024 18:27:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:93a8a8ce5f3c3d27f874a09163368c07de52f2266648f809ebe1b2ca4859fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba701a69d6b9b6a060c8bc3199888b730f877f741d86658d92f6de0f9147ba58`

```dockerfile
```

-	Layers:
	-	`sha256:59a351cf6bf8065cccb377b3ce0e9124f1401218e007c0b5935fa80713e4ef76`  
		Last Modified: Mon, 06 May 2024 18:27:51 GMT  
		Size: 2.9 MB (2934484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90656e90325c572d24cc34d27b51a3930d113d0d46a64d5080aa9a73348b914`  
		Last Modified: Mon, 06 May 2024 18:27:51 GMT  
		Size: 28.9 KB (28931 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:add608d8afe9bc6a5b99009e9852ca3b4ee12298dd06b38920f7633637edc97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70142879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6cd25cd98bf02d1fce07c17417dcff6571f62a30e7e2cad3e6b4c27a63e496`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1~bookworm
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     gpg1 --export "$NGINX_GPGKEY" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7295c0d28dd9fac6e79d9303f30abf164022f7ff6b1f4f5196b2c71a87bc5e`  
		Last Modified: Mon, 06 May 2024 18:19:18 GMT  
		Size: 42.6 MB (42625938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb5dd505131a2bd9965f991a5f250f92d20e8c296c05a4cd06aed63adee6f10`  
		Last Modified: Mon, 06 May 2024 18:19:16 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8b275cebb9d28c3ee5aac626327c5eeba703fb82c0905e91afadb19b552342`  
		Last Modified: Mon, 06 May 2024 18:19:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049d2e15136d64c1dd701768fcfbb970e0727f92094e772a65a1df6ed23268dd`  
		Last Modified: Mon, 06 May 2024 18:19:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0020184b61c33adc5d0ddc0ee5f83ea0abef85f2b2fade902e383ac1878d7354`  
		Last Modified: Mon, 06 May 2024 18:19:16 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b02e62eabafee8e8b35bedaaad65aaa6277cd1c413f2e65c1979163339ce365`  
		Last Modified: Mon, 06 May 2024 18:19:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:4d44d62c84e9be3efb81481258cbe9e3b3f64225c6bb359ee9ce277a00fe659f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2947863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59322d4b4d7e396451675c5ac3f5489fab9ea30ab22130a4dfff92e9b3c73f46`

```dockerfile
```

-	Layers:
	-	`sha256:2978f73893499de22e65170f59897ada31102e25ae66a3051483a0056c5387dc`  
		Last Modified: Mon, 06 May 2024 18:19:16 GMT  
		Size: 2.9 MB (2918982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b957b66507e3b24343333eef34c34985a2c9c169b7337a45cd533db46040c454`  
		Last Modified: Mon, 06 May 2024 18:19:15 GMT  
		Size: 28.9 KB (28881 bytes)  
		MIME: application/vnd.in-toto+json
