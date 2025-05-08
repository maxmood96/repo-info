## `nginx:stable-bookworm`

```console
$ docker pull nginx@sha256:0ad9e58f00f6a0d92f8c0a2a32285366a0ee948d9f91aee4a2c965a5516c59d5
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

### `nginx:stable-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:7d5e1be35e54874c8c6fea27d917002fffaf887eaf7bd12f3cb2cc7fa614cfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72382650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2dd24abce21cd256091445aca4b7eb00774264c2b0a8714701dd7091509efa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d563b4c3a3af6eea57a6cf046755a0ec366778d244fc8f7ca6ed77ceeeacf`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 44.2 MB (44150414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42be7bf60a09af4ea6946be81feb939c68daee4e63e356e9d70c14e9a932eb1f`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580b83207526cf1e347b5ee2b20a0833c91f0e150ffa4db5e186f9e213d186b0`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8b35505644b2828833c9e4785aee9b7850f324c9a55aac4798d02e9df0bb23`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f196c801e2eb61ee77f2b292987378ad718dd65e059fc71b08a70042e06e7a6e`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65eec8b3ab2dda365543bb0ff7034e47633f42f47d4bca7dd19cc4a596e904`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:c6513e5d4b1be4ea5cc03085fa7fe5db29874a87ba673416fe3e2c597f983c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3f5c1ed0843f60187e2b853bb430e353c547ca48bda2ec6e5fcc3fafb056be`

```dockerfile
```

-	Layers:
	-	`sha256:d415c8772a4d1edfd117cead0308ae37aab48a3351e54a52b56506b60493a2d3`  
		Last Modified: Mon, 28 Apr 2025 21:43:18 GMT  
		Size: 3.0 MB (2956274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100376531c94180a7dd4d2779dd608a1a0922e70d732be5cecd4021b068366be`  
		Last Modified: Mon, 28 Apr 2025 21:43:18 GMT  
		Size: 33.4 KB (33381 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:362b3dafd3435c591b8c5584caae35fe8fd55a39cf67065b40665cf6ccc04a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62513596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405b0a17610eed17098912f39ebaefab55860f9e8890300805de2026702bf3aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Thu, 08 May 2025 17:08:44 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e1c4191e819b3a82610f80346586d832136b8b96be18ba8975ba4679a07b7`  
		Last Modified: Thu, 08 May 2025 18:43:30 GMT  
		Size: 36.8 MB (36751152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b78c0a4166a9a8daaa4bd0a535888f50027bcd3a6108b2dee4665e6413c558`  
		Last Modified: Thu, 08 May 2025 18:43:47 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86840060f475b8c584405c0ea10611983da469d7ad6ada0e7f0c0e0ea1118a8`  
		Last Modified: Thu, 08 May 2025 18:43:50 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7834581a480dce7f88546e4d25e625b51b1e180fcef5eebc84131adbaee25036`  
		Last Modified: Thu, 08 May 2025 18:43:52 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e93e0afc04bbd786f57cd05e6c978877292c28840a0519edbfcd45482dd338`  
		Last Modified: Thu, 08 May 2025 17:22:56 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64008289f67bb2a62d585497fb96680dc8747a2afa5f2fc11aa0e32dbde245a1`  
		Last Modified: Thu, 08 May 2025 18:43:58 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:4083bc787a3ea0ceea900fe96c2275ba0d45ad0664a97b53674a15dd063b4b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61628afb3e2be6f67374cd957e960908b6a6c4fc134c80fd73037f8a4b145321`

```dockerfile
```

-	Layers:
	-	`sha256:ef7ab1c112dd3b7676fc5f69cc88a6b5d30c83413c648c46f36df8ad0e99e72f`  
		Last Modified: Mon, 28 Apr 2025 22:27:24 GMT  
		Size: 3.0 MB (2977465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2beed7e2d2729d46888656adbe775c170cc129114b20b9e50bd52b941a0e734b`  
		Last Modified: Mon, 28 Apr 2025 22:27:24 GMT  
		Size: 33.5 KB (33473 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:bddb4e860c32d62742ff26d23bbf6820cc53fb6b6bbc47628bdb7d13eb83faee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60905175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726e145966b9ba153550e32ab301cb5b1ec37e1164e2bc82732b069abf72d92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c259f29c8f3e5ce92b408d8b0d270f4b82e18161ff5bb95100c288c69eff4fc5`  
		Last Modified: Thu, 08 May 2025 17:23:15 GMT  
		Size: 37.0 MB (36962515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e29fe8a94e26176e56ffadd1c0faf1213a1fe58ea44a8194ba5a2cdb5d5d6d`  
		Last Modified: Thu, 08 May 2025 18:45:15 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c1b879ddab526064c4d8221f31c759da3c03457292ff6c2c1de555a6a9367e`  
		Last Modified: Thu, 08 May 2025 18:45:18 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80e666fb7c336314c8b9b29645ed85df671dcde53bb6947848a34f377cf583`  
		Last Modified: Thu, 08 May 2025 17:23:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23403f6c72fb988052e331e2c72009139d5757b6fab8e30469a0529cce49871`  
		Last Modified: Thu, 08 May 2025 17:23:13 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01745371fe8a6efb78526e92e827fd61ca9ce4172b8eebfe407ec9a88906d804`  
		Last Modified: Thu, 08 May 2025 18:45:28 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:c3d2102e9f9e6711d39c3dcff751e085ebf5869e3c0abd18a369f76aa24087b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723d8e729ceee54386d407b3de2a5c793df5cf2f95f8ba653af254c9bb054217`

```dockerfile
```

-	Layers:
	-	`sha256:7544f4ac6778869ad5e52f0f9f494ec2422e1130968d70cff0dfc7b1e9c3e04f`  
		Last Modified: Mon, 28 Apr 2025 22:32:26 GMT  
		Size: 3.0 MB (2976432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12332cab6465dfe0efbf58cb992f9e4527ba493a404a395a65847ebf416a25ee`  
		Last Modified: Mon, 28 Apr 2025 22:32:26 GMT  
		Size: 33.5 KB (33473 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:28546ab5662ae3edadeddbcc5db0c1b63037398686b13837e09d1a12924dc183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68823554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b1cb61bd96acc3ff3c695318c9cc691213d532eee3731d038af92816fcb5f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e982873808872c999f88f1b8055af9c08ecac3e6adf1c4553b1225e689155a`  
		Last Modified: Thu, 08 May 2025 17:09:17 GMT  
		Size: 40.8 MB (40752340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9578ffc9150a95b3fcaa6a47952361106499c9de1ffeeede80531c5173a05`  
		Last Modified: Thu, 08 May 2025 17:09:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914350da86b00c43e0b214e5faa9c0d156b2d3a3c4c56104b58db832d9e9cb9a`  
		Last Modified: Thu, 08 May 2025 17:09:15 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2830a0b8f55096feabff73393dfa17a4b00597e07251326e7c3fe54697aaf0c`  
		Last Modified: Thu, 08 May 2025 17:09:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd46642287e2c9b65b5aaaa180b9fc094c9cacc9ea60bec82caa61efaac57e31`  
		Last Modified: Thu, 08 May 2025 17:09:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863a3a2a749ddd28a304ac657429379a208ec75935ab97d50de8add50a4d179c`  
		Last Modified: Thu, 08 May 2025 17:09:15 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:a4ef2d57b215d7b27c113c5ea9d1b73a64a45bbc6b3179e347e6bb72f83cdf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d8093ba238b22d5db6c49826319200bb0f153cd6efc5e3ce72da3089a384dc`

```dockerfile
```

-	Layers:
	-	`sha256:b7a06a34dd43345e0d20aa3f6cf4d36f2c797993fa50532f0cf9bc5572b13f6b`  
		Last Modified: Mon, 28 Apr 2025 22:39:33 GMT  
		Size: 3.0 MB (2956677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875894beb9b2f40a1e2d003343b748c48c1abf738f16d89e78c1a97b0c0f67bc`  
		Last Modified: Mon, 28 Apr 2025 22:39:33 GMT  
		Size: 33.5 KB (33508 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:8aa90d573a33796285d6cec9c825f7d24a6ea9b84e6dfcedcab7cca247ec8c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70752265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6c1222b0b2d0b4ec8506d303a5dd63c8a6bb0e7fe465e02a9daeb5fefb4c7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11161cf131f49027afdda0a18ba017da8f8761c74edb66b26724af5ca30a25d5`  
		Last Modified: Thu, 08 May 2025 18:49:09 GMT  
		Size: 41.5 MB (41536799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f2f5ff9b4e7aef1bc547ded4ac25680b167adfbf7fd9f17060e5baf571326c`  
		Last Modified: Thu, 08 May 2025 18:49:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d9a384c6e6b7b15be7610c5871798a6a8ca1e54d62c0e24e0bf8a7dfd73e0`  
		Last Modified: Thu, 08 May 2025 18:49:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96ecbdbf1e7899b9a2619e15530e19b9c470088db27769b783f8a6cbfca1026`  
		Last Modified: Thu, 08 May 2025 17:23:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e138e28c4ab142d71a3dd4b94fd710717fed00d2ffb3f7034ee308e008476a0`  
		Last Modified: Thu, 08 May 2025 17:23:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ccd9e6efb9cbc3299c346f81541cdbc183cc56ec5adecbd7575ab3c3402eea`  
		Last Modified: Thu, 08 May 2025 18:49:45 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:898f67a84cb3643fe4d6818832805f8907599d694d286dac501dc929e5872632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3002904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fad82e43bdb4e15a23efd7608d780040355db7256b3c19cad0c2287c79777bd`

```dockerfile
```

-	Layers:
	-	`sha256:c24e527ff00d39b9c81982de1ea9b8665471949074ca371577e659b6ac71c33e`  
		Last Modified: Mon, 28 Apr 2025 21:47:20 GMT  
		Size: 3.0 MB (2969565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37397ca6d142a63f50f835732011f1f5594fa23198193f5c63878c429bc49895`  
		Last Modified: Mon, 28 Apr 2025 21:47:20 GMT  
		Size: 33.3 KB (33339 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:4c279a85edefc1ad8f4b508a3a4581c349757f5af906a65e810bace086a84e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68455471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc58c8656406990877eedf791b58300b0103f10b7d3315e08a77274649312ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99680e5e2650b1f1b65e911801e0994f57a50391b2908892bb0c8b5cac18d0c8`  
		Last Modified: Thu, 08 May 2025 17:23:10 GMT  
		Size: 39.9 MB (39936722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e875282098724f84831d691caf4935aca9459f6a82b3efa64d29db2524a6b92`  
		Last Modified: Wed, 23 Apr 2025 19:15:06 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb12086c874c0ba12a2c4ab477dc3b4ec8abcbae34c76e796d12a3d87145140`  
		Last Modified: Mon, 28 Apr 2025 23:31:56 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150976d15cf704666a73b5eb917b062229274f79cef93a1f62fe590e0b4cb27d`  
		Last Modified: Mon, 28 Apr 2025 23:31:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fee531f545f540de78ff0fbd5823dbf57a41b8629e1371ca8b9148aa13f1f87`  
		Last Modified: Thu, 08 May 2025 17:23:08 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c056b91cdc45e9374ba5673970c1e25c432f8cb165087ce5cda130bab7fd9b`  
		Last Modified: Thu, 08 May 2025 17:23:09 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:58b68bc72e63d547c7cb2490ffca6b566be35f6903ce2dffe3f9327a00d81a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db6b3b54bc801e87a33729d7bda7a080044e2c55e6c0fcaa214b91e0cc4a3fb`

```dockerfile
```

-	Layers:
	-	`sha256:f1ab4fa47fb169dae986dd2cff320b076f832aed14bc0db2797d70e479d40179`  
		Last Modified: Mon, 28 Apr 2025 23:31:56 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:4a4b3883431af9fde7364b110023f4ef6f14acb1d5db82b7d336c4096ea43878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77101527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c51da87550d7a3b0c9947f7695d647891878c1649335cd135b3cce8187bb9b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d04a8a128ec733e2a08c32f6d4a5e4c84aa764afc54fab28f165dcc53e993`  
		Last Modified: Thu, 08 May 2025 17:23:18 GMT  
		Size: 45.0 MB (45028484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181834a85c945e3f627c44311dc6e1e44261beaf084b1bf4a2d18ed0e706834e`  
		Last Modified: Mon, 28 Apr 2025 22:24:33 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6636af273e0dc53d653a81ebbeadf7cdde47693d522b304335963687e379e03`  
		Last Modified: Thu, 08 May 2025 17:23:09 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbfdbd9a505409f3da413fb63e04fe603f6c494ce14afef719070d69f52bcc9`  
		Last Modified: Thu, 08 May 2025 17:23:08 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f909131ddc8d01564e224af65898681b424c4f097cdddc416cda72f61f442434`  
		Last Modified: Mon, 28 Apr 2025 22:24:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4351e368976254c2d705215a96599eb4d9712ce859376a8fc7a88b49c01dd6`  
		Last Modified: Mon, 28 Apr 2025 22:24:34 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f011ea3486b00cdb07521c90cbaf3c5c2f01d0b37f53815847a2e87d29c84581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3017468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc05854423b53c331c37aa01c54a5b64ae06b40e23a2c51abdc3cacca15afab`

```dockerfile
```

-	Layers:
	-	`sha256:3c9098c2fcf8b3d53444cf70a24d50df0fab51c745ed90592de5b3d188f06c43`  
		Last Modified: Mon, 28 Apr 2025 22:24:33 GMT  
		Size: 3.0 MB (2984031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad32321e317edd93484f3d4c60bf215e8fab53353573d53ae1058fa46a038cd`  
		Last Modified: Mon, 28 Apr 2025 22:24:33 GMT  
		Size: 33.4 KB (33437 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:a8ac4f951888f2b1e15be3c6c56a6434dba30fa661a3c8da5840e438d00f3dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67071374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f510cb463c59abcdcca3dde16f596b72dbbee208dcd4c9a6cdd3374201ab0159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c814a3cf7eea4bf639644965934babb7e3199e9df0e79460ecb6fd09479800`  
		Last Modified: Mon, 28 Apr 2025 22:07:33 GMT  
		Size: 40.2 MB (40181901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85da1937ff64c631159659c1bef7b138b087553dd6d3828313a9cc065f24f721`  
		Last Modified: Thu, 08 May 2025 17:23:11 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3bbd23d8ccc3ae0879752c172cddb79cc2c1bed9728ff35a5e1d1233aa4447`  
		Last Modified: Mon, 28 Apr 2025 22:07:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aabe85adfab7647d51004f113ab3807ed1a93eb4dc7d57bd8f2f4210d855000`  
		Last Modified: Thu, 08 May 2025 17:23:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5898d1332f8cabdf3d4558c505c57fa554837acce13d46aa16eb219cf7b607`  
		Last Modified: Mon, 28 Apr 2025 22:07:33 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d96b1f09b412b8d60ba0ec0470950d860d61f92c6aab08340ce00c04a7d96d`  
		Last Modified: Mon, 28 Apr 2025 22:07:33 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:10731cc4bb4f62c4ad3239c775012e8920fbfbc6c68cdea348dd5f8878b932fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ecf150026909c0e86363351a798ae34edd6e634fc2fe555f7ad635167012`

```dockerfile
```

-	Layers:
	-	`sha256:c40dd9a995381fccad3ef3ddaadcf432bc77f826c506555ea9051bbe28cabe34`  
		Last Modified: Mon, 28 Apr 2025 22:07:32 GMT  
		Size: 3.0 MB (2967667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a3cfc61c8cc1e4adad85aad31133da8e8264de8009602927592ad03cb4c757`  
		Last Modified: Mon, 28 Apr 2025 22:07:32 GMT  
		Size: 33.4 KB (33380 bytes)  
		MIME: application/vnd.in-toto+json
