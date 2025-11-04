## `nginx:trixie`

```console
$ docker pull nginx@sha256:1beed3ca46acebe9d3fb62e9067f03d05d5bfa97a00f30938a0a3580563272ad
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:trixie` - linux; amd64

```console
$ docker pull nginx@sha256:bd1578eec775d0b28fd7f664b182b7e1fb75f1dd09f92d865dababe8525dfe8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59752743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d261fd19cb63238535ab80d4e1be1d9e7f6c8b5a28a820188968dd3e6f06072d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:06:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 04:06:21 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 04:06:21 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 04:06:21 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 04:06:21 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 04:06:21 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 04:06:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 04:06:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:06:21 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 04:06:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 04:06:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266626526d42cf7fe5f56b933db3f4c59c0596b7e2c3a556ba5ec4981daf3e9d`  
		Last Modified: Tue, 04 Nov 2025 04:06:39 GMT  
		Size: 30.0 MB (29970043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b0949be89766f7c6a8746f1971021a8e8c84928af00454c0f9c6e38ebf54c`  
		Last Modified: Tue, 04 Nov 2025 04:06:37 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921c57c6a81addac6ca451906699ca6ee8c01fd708805a928181c5370b0a30c`  
		Last Modified: Tue, 04 Nov 2025 04:06:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9def903993e4ef9a3faa02bb893b0382768a4d466d51247bff1ea80b119377a1`  
		Last Modified: Tue, 04 Nov 2025 04:06:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bc359bcbd74bb3d11b94cf3c6d94bcf9bd2d3e450483fb978124ceddb9ca57`  
		Last Modified: Tue, 04 Nov 2025 04:06:37 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8e296d9df1dd5e2ddc81e5e758f9762fdb932e982ac6873e36692c3e3c983`  
		Last Modified: Tue, 04 Nov 2025 04:06:37 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:0c798fdea148c2a4aa684526de6dc2baeed661e364ac2ef3f2ef7693fb1c1029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930b781ce693a786832b8a6e169db14abaf1298bac5059947a0ca9f052a36505`

```dockerfile
```

-	Layers:
	-	`sha256:4be20fe4ce96400bdc3337d23a57cfff94c046ceb79da234d0e9ddf06b6cd1cf`  
		Last Modified: Tue, 04 Nov 2025 09:50:39 GMT  
		Size: 2.8 MB (2811715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82cb8fb18089f9c8b945ba9cd97664ce1f6aa6fd8b8fb250aa4bdb0dda41e70f`  
		Last Modified: Tue, 04 Nov 2025 09:50:40 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:5dd53c4c2197dda60eec710dee3496b37b54745745e770bf7ba5841390edbae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51363463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6a53a5259e72e67fc3a91d1a6a324e6d06db85b9ba7738dca794f164f69ac5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:30:03 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 00:30:03 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 00:30:03 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 00:30:03 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 00:30:03 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 00:30:03 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 00:30:03 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 00:30:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:03 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:30:03 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:30:03 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046cfa5270909f28dcad9d5e04db6762b7c0da3eb86237ec5fc9a2d48a63c698`  
		Last Modified: Tue, 04 Nov 2025 00:30:32 GMT  
		Size: 23.4 MB (23412423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6553d6a9a1b8ce359df11c4cbd84c3ff220ab92e7362ff8b35a884ac5f33dded`  
		Last Modified: Tue, 04 Nov 2025 00:30:27 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b197bfb26bff83649faa8aecafa391f48847996292413304a64141ab0fee80`  
		Last Modified: Tue, 04 Nov 2025 00:30:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb855f6984beee2656a0e9d00a36de5828e9e4a7f95333a3efb6d6d66e77357`  
		Last Modified: Tue, 04 Nov 2025 00:30:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0450f006ba416570b55e037199d4f1090529da89e118f93985a74634aaeb40`  
		Last Modified: Tue, 04 Nov 2025 00:30:27 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97263d26bd6cfe70d1f67445b5a8d1bacf793983a60eaa10e443d89bb9063099`  
		Last Modified: Tue, 04 Nov 2025 00:30:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:4b2afec60ddfb19ec75f5fb15a055a9b2671b7a344c48815b43098dd5b1bfed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1835461cdd658e70e098ead92a130cd5cd97e6f6dc752c876841046fa171d352`

```dockerfile
```

-	Layers:
	-	`sha256:574092aa00ee59ce80ceee704ffde65a8ab4483b8f738c97d5f99fe7a2cac394`  
		Last Modified: Tue, 04 Nov 2025 09:51:21 GMT  
		Size: 2.8 MB (2837855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b3e08c22451c460034e0ae6d8eef0bf1d01ea061c7bf77f4e231d0f28b24df`  
		Last Modified: Tue, 04 Nov 2025 09:51:22 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:e7b13d0becb2bfe336926aeb4f762debc2a3ba0ece7b2d48910fe5c94667aa9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d05a13eb7a31ad3d73ae48fce313eaa05b7c5a582eafb9c288b0f8c68e93073`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:11:47 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 02:11:47 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 02:11:47 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 02:11:47 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:11:47 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:11:47 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:11:47 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:11:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 02:11:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 02:11:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484c4f4c2a5f3332078d950328f7fad21d14e5914dff8033c32e8704001a6c7b`  
		Last Modified: Tue, 04 Nov 2025 02:12:05 GMT  
		Size: 23.4 MB (23413091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf027775b62a700cf8d7346d9c6929361c4da50988b4d503335cff50934ff8d`  
		Last Modified: Tue, 04 Nov 2025 02:12:02 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85ba2cf95a9996bf9b113942e81cf55842d3fbb2935fb14fceefa1de08e3f8`  
		Last Modified: Tue, 04 Nov 2025 02:12:02 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dab308cbb11ce1ce94810b89115fd7a2f96ac70c0edf5a751d65eb62ed8f53`  
		Last Modified: Tue, 04 Nov 2025 02:12:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6458abb752cb9e8cba7b640c1d09584dfc6b85813b42034b68d2e94dfaa74cd3`  
		Last Modified: Tue, 04 Nov 2025 02:12:02 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9e40c759bc659c2b7c35fef0f8713713dfa9303fdc261b45f10c457c3f1bf`  
		Last Modified: Tue, 04 Nov 2025 02:12:02 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:e43007b688de2eab645b9c679cac0aadcab6f5658077cc218c75d7f3b81dfff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4810a03aef887a9682b3509777e358f41e3a891920ac436e88fcbb39d53759dc`

```dockerfile
```

-	Layers:
	-	`sha256:0421fb71c27a08ce8bb514eb5a986e900678d136c4c77963a9a4aab27ae57580`  
		Last Modified: Tue, 04 Nov 2025 09:51:25 GMT  
		Size: 2.8 MB (2836600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35086ffbe1f8b7175ad1bfdd9601e0344b55ab8b2135b73c30a807df07c41ca`  
		Last Modified: Tue, 04 Nov 2025 09:51:26 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:63a931a2f5772f57ed7537f19330ee231c0550d1fbb95ee24d0e0e3e849bae33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5a8f08b76da55a3731f09e696a0ee5c6d8115ba5e80c5ae2ae1c210b3b1b98`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 01:17:49 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 01:17:49 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 01:17:49 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:17:49 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:17:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:17:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:17:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:17:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:17:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 01:17:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3a535ffc2fc56da973314114adbd69373bdac6e65518ccd973a2048ad35417`  
		Last Modified: Tue, 04 Nov 2025 01:18:07 GMT  
		Size: 28.1 MB (28099430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b6d209211fb260cdff87a10b238a1579fce76ddcfbbabbafde4d25884ea7cb`  
		Last Modified: Tue, 04 Nov 2025 01:18:04 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59679015de7391a6955f9bf5ee9531bfaf9664e1d2115923b34b7e211293e90a`  
		Last Modified: Tue, 04 Nov 2025 01:18:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469ebd60c79c6238255a6840462db9ae9d70215686d1a88e81d12059bd19a2e`  
		Last Modified: Tue, 04 Nov 2025 01:18:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9f1af9e100b2c641e0164d20cf287cc543dc01c10e39fe8fb26d20800178e`  
		Last Modified: Tue, 04 Nov 2025 01:18:04 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184706839d41a7d155b6253ac733e6eef75f4e8a61b5ebb13ce8f17e9baa27cd`  
		Last Modified: Tue, 04 Nov 2025 01:18:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:36198c74d4f6dc69c85e84e08bd575423cb2b8734036e0c13d13d0ef8c575d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc6f4d94213b6622a0ab012b5cec3ce5c684babfc42c9682b6834964f9bf90c`

```dockerfile
```

-	Layers:
	-	`sha256:121959bb8c597643233b2ce764a8ef13350c6487868cdced002287d40806ce61`  
		Last Modified: Tue, 04 Nov 2025 09:53:55 GMT  
		Size: 2.8 MB (2812199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54c8ec2044c7f6d8457a42ef4ecab79f28a848800c1e1dbbdcff24e96ac2d11`  
		Last Modified: Tue, 04 Nov 2025 09:53:55 GMT  
		Size: 34.7 KB (34720 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; 386

```console
$ docker pull nginx@sha256:ac27e318cff1c5340d9a2c2d8db5f0a374dabfe1f285f81348008e01bd980d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59991067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c649b34579c60ed09ee9f279b26a9b501ecd3ce8377f374abdd04b1ad28bbb0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:24:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 01:24:19 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 01:24:19 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 01:24:19 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:24:19 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:24:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 01:24:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 01:24:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:24:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:24:19 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 01:24:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836996eed9e0296831fda77e91e47ba9880117f0c2fce86d70e2c227bfee80e4`  
		Last Modified: Tue, 04 Nov 2025 01:24:38 GMT  
		Size: 28.7 MB (28691687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d156ef607d76f09089fc4c0d016092907d758fd83e3eff501ccdfe97b3fd8e46`  
		Last Modified: Tue, 04 Nov 2025 01:24:34 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0119783faa29eeb020fbf94f1e8b2954baf6d61a6b7556a9f9f62ba54a92bfbe`  
		Last Modified: Tue, 04 Nov 2025 01:24:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21114a5b09d1d53de0edb661a2ebe882f4040b1f15305316d498564781f2e33`  
		Last Modified: Tue, 04 Nov 2025 01:24:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d2002991b0895420b18fd048ca8ed08e0da160662d9f73af06cf96f9a4cd8`  
		Last Modified: Tue, 04 Nov 2025 01:24:34 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc305a41e2aeb3b3382bf3f1522557da9a7cc8d5f4b5741c54dce4f798d98e4`  
		Last Modified: Tue, 04 Nov 2025 01:24:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:dcb4b9a4f4b0547645addbc05a7c6a9fbed5c06bc68521875cdc6be518a4afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659003c922ef439e65aa8bdd5f2278f1b50cc339255f04497c14fedd78a6991`

```dockerfile
```

-	Layers:
	-	`sha256:e57dad1c121ec04dcd30d8215bd85846e109b4dcc2d809d30c266742f1ce1c10`  
		Last Modified: Tue, 04 Nov 2025 09:51:32 GMT  
		Size: 2.8 MB (2831551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72eba9ba1b15766fdec50a72c948391620f9b1693424dbc5d9853301f721113`  
		Last Modified: Tue, 04 Nov 2025 09:51:33 GMT  
		Size: 34.5 KB (34482 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:9e20a218b4054bee7c688bb34c86de076f44fc8c85d51fa93a567dd62bb7225d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63818976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98746d96c61f84f5382d464ec99aaa9e71f36c1847625da6d7c7809c562f6fc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:03:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 02:03:48 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 02:03:48 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 02:03:48 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:03:48 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:03:48 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 02:03:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:03:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 02:03:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:03:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:03:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:03:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 02:03:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:03:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 02:03:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 02:03:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c56a4d43d614034387b709f7ac56e457f2e7f4bf8d0c4084a7345939144649`  
		Last Modified: Tue, 04 Nov 2025 02:04:45 GMT  
		Size: 30.2 MB (30215724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724f3f6ce61f59d7e07c05493fe4e31bba3644b4bf0e0cece0c3c03e6b71c78`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1d46ece80dbec517db10d7b52cee102c372155ebaa1047be579ba968afd767`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f0216c678ff39826df4e3f2d03240e0875b0ef178ef8fac9ee527e91b153bf`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f12ba8a6536c7bda37a1f337c23fe7c4db6797e24667c21035ff5514ca2cde7`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943ecfe3f375b5c7c84114f45bb574018b620b5f373b2f6a37e78bc6132211da`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:bf59f6482ee5ca10fa33ffb269872719ae1b536bfe24cee02e2c4e0959b048e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2548972aa05288d0212de2fe97eabf080eb8bc8c537feb9f8205b6fc9d4473`

```dockerfile
```

-	Layers:
	-	`sha256:18d7d1893b8b5d4ef87a208e9018991f13bfc7352f7c256ca062514af7720a72`  
		Last Modified: Tue, 04 Nov 2025 09:51:36 GMT  
		Size: 2.8 MB (2839245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9338e64937aa5498c29b09ab1e0aaf98929dd2e24d977a9a1ba663b0b8c3b16`  
		Last Modified: Tue, 04 Nov 2025 09:51:37 GMT  
		Size: 34.6 KB (34624 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:61da52d2a49c2e8db79132503f5e40796c13644843e9fbf5f9858fe415517936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54688364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d5f7d497ae1a7c04a1c996a581f75c8e0bb5b7bb368870a9cf1177014a5d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 05:49:29 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 05:49:29 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 05:49:29 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 05:49:29 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 05:49:29 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 05:49:29 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 05:49:29 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 05:49:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 05:49:29 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 05:49:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 05:49:29 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a62c5c3e8d9139639dc03285d2fdb91e97bf800d8f0931a1b6e742eb0085ed`  
		Last Modified: Tue, 04 Nov 2025 05:51:04 GMT  
		Size: 26.4 MB (26407968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdbea323d4b691957309ae4a10d54b61686d87233296cee9f880048c7c3dc9c`  
		Last Modified: Tue, 04 Nov 2025 05:51:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639235eae7828853bac3218d520b3644765e9002296e18f9bd4b552d32f0ae42`  
		Last Modified: Tue, 04 Nov 2025 05:51:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c617c53f3e9c493026c74f843aee59a5a905202cb5f3204443260df880bfec`  
		Last Modified: Tue, 04 Nov 2025 05:51:03 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2d13e228575267bc708bdbc703e49017cd583ebf076302f7e7a5a666e84220`  
		Last Modified: Tue, 04 Nov 2025 05:51:03 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21316bb4d170918002341e9622ce9ef3f89440dfc37d3838950411607b2bb31`  
		Last Modified: Tue, 04 Nov 2025 05:51:03 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:649388a8bee7af8b33030867a0e2f7245065a8ee0bf7bd30e83b9f64fe27208a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2863656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87f02045e33cf5b707e31a7724bcfb212aa1d86b11a470cb46e7e195588253b`

```dockerfile
```

-	Layers:
	-	`sha256:bdca1846d42e4f2f6c7b115ff5b02bfa3d92b30cf2cfdd7077c865b556e5dcd6`  
		Last Modified: Tue, 04 Nov 2025 09:51:40 GMT  
		Size: 2.8 MB (2829032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947157b3b3d0f4205cb12bcfbe6c4d316908dc2c3b6c738f652f985b1d2acc5c`  
		Last Modified: Tue, 04 Nov 2025 09:51:41 GMT  
		Size: 34.6 KB (34624 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; s390x

```console
$ docker pull nginx@sha256:80d64129dd9588ab5e1969cb58e46e90b9f3944408e3f4811c3a18958da7e941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56974086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a36bad01703ee01c5b1e0ee59785170570da1f2ead1f036083378c7bff1055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:06:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 04 Nov 2025 07:06:56 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 04 Nov 2025 07:06:56 GMT
ENV NJS_VERSION=0.9.4
# Tue, 04 Nov 2025 07:06:56 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 04 Nov 2025 07:06:56 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 07:06:56 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 04 Nov 2025 07:06:56 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 04 Nov 2025 07:06:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:06:57 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 07:06:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 07:06:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc24aebb54fbd45342dbb8807ceba4dc3053f3de02c9b2d0f69773be1c911bc`  
		Last Modified: Tue, 04 Nov 2025 07:07:20 GMT  
		Size: 27.1 MB (27132094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c8b49d13c6a0866fc0fa2f4e9f3b9501094170b5376cce733785f85db832dd`  
		Last Modified: Tue, 04 Nov 2025 07:07:18 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032f59aa81b67b47f4b00d15b426c59cb750b00ed6d103a3e9aedf4bfe9a9a4`  
		Last Modified: Tue, 04 Nov 2025 07:07:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5280f3290f0e3d90e8688c3cdb956bdb357eebae816f63cc3dd9d67628463444`  
		Last Modified: Tue, 04 Nov 2025 07:07:19 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab345d4bebae3a8ae3fc9133ed201ea2b6239a6db7b2c6a919488774a7b4f72`  
		Last Modified: Tue, 04 Nov 2025 07:07:18 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c83f6c8f5d7ea1951b5c1538a18290628710b8e53f6fee68f4b3bcff72fe80`  
		Last Modified: Tue, 04 Nov 2025 07:07:18 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:0b43f48991de9b554893968d8e0b6fcd5a2aaa82b36d98b91246eadcaeeead97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2779545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6664a277c695c21f6bcbc432325ac97128ab8c9cf2b50178e806847de5ddbd31`

```dockerfile
```

-	Layers:
	-	`sha256:f71b29d3889c6d5f975ad15425109bb5ff2bbe98f2a1d5ed483a21d9d0954ff8`  
		Last Modified: Tue, 04 Nov 2025 09:51:44 GMT  
		Size: 2.7 MB (2745001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4beab21ba734be64a028bd1bb433af7b368109c37fc66a934d3dde809b6e62`  
		Last Modified: Tue, 04 Nov 2025 09:51:45 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json
