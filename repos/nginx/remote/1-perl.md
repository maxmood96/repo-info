## `nginx:1-perl`

```console
$ docker pull nginx@sha256:5f4cf3e05baa997e7ac395dd20ca80a5c69f722bcaf9f5ef9597e0e294a96a63
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

### `nginx:1-perl` - linux; amd64

```console
$ docker pull nginx@sha256:30669850b725f3e3e64e6b270db74bf37f59fd3833585f4cd7a4ba5b50a2d820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71912420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7615c975fa1fd09bb6ce08b34cafeb2f26f238eaf7ba5114e2abc1d5f34cabba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 21:50:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 21:50:05 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 21:50:05 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 21:50:05 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:50:05 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:50:05 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:50:05 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:50:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 21:50:05 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 21:50:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 21:50:05 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:10:23 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a6ab1415585a8dc626877b8de231086ab4d45ea8709d35b8ac7ec24bea3038`  
		Last Modified: Tue, 28 Oct 2025 21:51:21 GMT  
		Size: 30.0 MB (29970138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e86847a3920c130e5f7e66bdf15b66b9ed5426b80ecf1b2f8e7960794620a63`  
		Last Modified: Tue, 28 Oct 2025 21:51:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bace208328954ff24f16c62a7492c4b3a4d9451a10f23631417f3feebe3f44d`  
		Last Modified: Tue, 28 Oct 2025 21:51:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89df300a082a0f5d71c8aff1944dc57a49544592d8d804fe7c61b7e844aa80b8`  
		Last Modified: Tue, 28 Oct 2025 21:51:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb9ffa6621d9044c7062eb2fe4b181ce919447e2575a8577dcedbd7aa5aa67`  
		Last Modified: Tue, 28 Oct 2025 21:51:18 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5545b08f9d26518aae35920f1c1b7cdf962b32b69e9feba182bfb3e0b90dcc2c`  
		Last Modified: Tue, 28 Oct 2025 21:51:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d47d090a8cfbbe33b0d10c851370c7e3c660011ed6b01a0a061e0ec5ce83dde`  
		Last Modified: Tue, 28 Oct 2025 22:10:46 GMT  
		Size: 12.2 MB (12159764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:1e3abf9a42640cda8275e289710ea8db3c35728581e13f2d5920c3dffb5379fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4259358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd496cf6b4317a6e67312ef5f8a1617aa9f85fa45c35e8fd872d5d6f4dcdfc04`

```dockerfile
```

-	Layers:
	-	`sha256:7ca241404a92f1a6ac51cdb4d804a36945e97ec99ac0111d4d01b2651bd75a78`  
		Last Modified: Tue, 28 Oct 2025 23:52:18 GMT  
		Size: 4.2 MB (4235135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aecf02f05f3f25668ad20cd2fc341fb7c24fd4628044ffa3b421a098c8412ad`  
		Last Modified: Tue, 28 Oct 2025 23:52:18 GMT  
		Size: 24.2 KB (24223 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:e8710fef21e68ed17e0e3310058c000857c1fa8c86630820dd3bc0321074bc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63305225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2151c2d91705f47cc1b29e686c2cfa9588b36935b68b52f6e7fd9bc3474e3c59`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 21:53:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 21:53:08 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 21:53:08 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 21:53:08 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:53:08 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:53:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:53:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:53:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 21:53:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:53:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:53:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:53:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 21:53:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 21:53:09 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:15:05 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa65c8e67a157fad2d0421b8cc7fe80d35cc044ec63af2315e7e34f2d948857`  
		Last Modified: Tue, 28 Oct 2025 21:53:28 GMT  
		Size: 23.4 MB (23412430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf24133fc40fbdfff21edea9584e71460a50e1c38d26acec799dda8e62dff5d`  
		Last Modified: Tue, 28 Oct 2025 21:53:26 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c99968870ec041f21b844aa7550cf646f8aab46e409527199507806cb7c3a3c`  
		Last Modified: Tue, 28 Oct 2025 21:53:26 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca9786857554f2d7cc07cf400d206aca3834d5775161c6af5d92c2f5270dee6`  
		Last Modified: Tue, 28 Oct 2025 21:53:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd970f6c0233929e48af09741dc0c4123521ac849062a73e3f7f7b7e3e403f9`  
		Last Modified: Tue, 28 Oct 2025 21:53:26 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb30d6d42bc5f26aa9642e1ab71281308fe738d32b9b47fc9e6f225a8807ca`  
		Last Modified: Tue, 28 Oct 2025 21:53:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f545d0142d2632c3b1898faeb4b1e33760ce69b581562036aa15eb75ffd73a`  
		Last Modified: Tue, 28 Oct 2025 22:15:24 GMT  
		Size: 11.9 MB (11941927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:2d7db3296ee75e117f06654938c9652101d905a37d0e3edbf6bdc7bb7476bb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71a5d9e12782f32f6ce236ca7a66b71d74ede8afff7ecfdbdf128f3e8bcbb47`

```dockerfile
```

-	Layers:
	-	`sha256:c7995f5c5ac079b58750b667d8664fa944ea25890ac5dbddfa3b97abac570f0f`  
		Last Modified: Tue, 28 Oct 2025 23:52:23 GMT  
		Size: 4.3 MB (4267192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e665d5bba820dd462d3e0b9471e9876684e650c5d0c4d8961ec87a2be235c6`  
		Last Modified: Tue, 28 Oct 2025 23:52:23 GMT  
		Size: 24.4 KB (24351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:52606361aacf569ba38c2bed1aade0907e6dfd7b266ef5089f73f63642478740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61382743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8e4bd88a00571ce7d1e73349edd2fdeaea0efaa7e916f66597bb9ecbbd861d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 21:52:23 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 21:52:23 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 21:52:23 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 21:52:23 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:52:23 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:52:23 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:52:23 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:52:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 21:52:23 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 21:52:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 21:52:23 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:10:24 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9d5d9ab394ed3bfba3b0d2b257eca30d62bb3367389d0a5081b5d5f494e118`  
		Last Modified: Tue, 28 Oct 2025 21:52:41 GMT  
		Size: 23.4 MB (23413073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c1225b93f005698428e8c3414216fd33ba81c15ae23e8ab76adcd2521b8306`  
		Last Modified: Tue, 28 Oct 2025 21:51:42 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c34148adcf24f7d1c1a85f4de62389c89e79c404cda2a7861f804211e8e49a`  
		Last Modified: Tue, 28 Oct 2025 21:52:39 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da15bd9933256539b52fd5a87802f3389cc043531591cac472b9922682dd81`  
		Last Modified: Tue, 28 Oct 2025 21:52:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabadf484867f7cd591d4a9cec89e90abb2b239f013128f7c953e0d634315495`  
		Last Modified: Tue, 28 Oct 2025 21:52:39 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3ae911a4dce57d0c8026a39a6d7931cb932a6fe1e1c54959e4d2c8b42802db`  
		Last Modified: Tue, 28 Oct 2025 21:52:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d25f7f4a134865bbbbcbe83abb1faa7609d41fde13cd15c462fc210fa85364`  
		Last Modified: Tue, 28 Oct 2025 22:10:46 GMT  
		Size: 11.8 MB (11752174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:948d46859c963d76689d01f8e0d5fa94047adc9a279a3512ab79e1696abd686f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8126fead5ec4c982b9b7a06fb01ab554d0e8f006ba5dc6bf6b397ddb2a7e5d91`

```dockerfile
```

-	Layers:
	-	`sha256:7dec0e838eac1d15e170d7ae8adca9669f29b364069256d27d8b41f99589319b`  
		Last Modified: Tue, 28 Oct 2025 23:52:28 GMT  
		Size: 4.3 MB (4266713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b9900fcddc483f983da03bc9f4b92bdaa696ecefea0006c606850ec317f18b`  
		Last Modified: Tue, 28 Oct 2025 23:52:28 GMT  
		Size: 24.4 KB (24351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:de9406e087669f5e3945dd34f0e59246b2c500689ce0f4b8f4ff7d3192c7ea93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70340468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f7070049b262d1534d0fffa3f9294b68c60c2d8108f58bb434a34dae3ef3be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36a0ddcec2e8c9d5a3491ea337d33bdca4528ed7389329ff937ddcae6a0a06`  
		Last Modified: Tue, 21 Oct 2025 01:21:33 GMT  
		Size: 28.1 MB (28089580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdaeaa5c0af3db6c0a7518083830a61688ee9021f5d3cde406f4e5a99c0d5a9`  
		Last Modified: Tue, 21 Oct 2025 01:21:30 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bac28be26c7bdb16e79915cbc03eb557e8c8eb53dff39c6a8e4c3ea62c5bfa`  
		Last Modified: Tue, 21 Oct 2025 01:21:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5194df169f983b85a4fc38c6071dc2a76df6247abea40ba68787bfc7fe49d5b`  
		Last Modified: Tue, 21 Oct 2025 01:21:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0ad8dd4b14c9ba8d35ee2b7149900dd028619b9a89e1c43d138ee03b343243`  
		Last Modified: Tue, 21 Oct 2025 01:21:30 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5ca44b0ca16a1dd8a54bab63174d0bdb1940d1696a8d7ddb4017cee5e94c70`  
		Last Modified: Tue, 21 Oct 2025 01:21:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d416fad64df2149584f00a9576eb383fbe9bf93307223aec45b3d0b0d32ebb45`  
		Last Modified: Tue, 21 Oct 2025 02:31:58 GMT  
		Size: 12.1 MB (12104184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:ae53c1eca453e940697a98a9cdda311741529d5366eff1452703ea53af5c5d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc3bfd35388a91a7be1cc142159e2a7a042d11a12445b78859bf75bcab1e9c1`

```dockerfile
```

-	Layers:
	-	`sha256:dde5ee3c4980a9fbd67c075504486a1f2a6d977f2d893a5152393b5e8a1e8b86`  
		Last Modified: Tue, 21 Oct 2025 08:51:26 GMT  
		Size: 4.2 MB (4241661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4743979c9f7b37586f474cfc49cceea75e86d95b7b1d169324d7e5b26b34ad`  
		Last Modified: Tue, 21 Oct 2025 08:51:27 GMT  
		Size: 24.4 KB (24442 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; 386

```console
$ docker pull nginx@sha256:a8b3875e915f544cca9196ab1d4bfdf30cf1ff3e5c77fba2c339071a85094f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72168886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef78e56a4dcaba681591360dab321afc0a9d91fe8cff9d9ab9b983df209eb6fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 21:51:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 21:51:26 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 21:51:26 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 21:51:26 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:51:26 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:51:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 21:51:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:51:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 21:51:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 21:51:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 21:51:26 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:12:22 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c89623dd4b124d9d054df246a874ded36503d524274b584109b1db4025aa096`  
		Last Modified: Tue, 28 Oct 2025 21:51:44 GMT  
		Size: 28.7 MB (28691672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c1225b93f005698428e8c3414216fd33ba81c15ae23e8ab76adcd2521b8306`  
		Last Modified: Tue, 28 Oct 2025 21:51:42 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a5f903d0bd4149b014b75eec4a8b88854d1445cabc619ffccb64ff1053b39`  
		Last Modified: Tue, 28 Oct 2025 21:51:41 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cf9be72f2a98b0fe114672eddadcab519545c975e75d982ea60b785c59bd37`  
		Last Modified: Tue, 28 Oct 2025 21:51:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23831b8c4d329d3b816fb90e9f5ff210b6159c8e1f25d8c18e8ede880dba73`  
		Last Modified: Tue, 28 Oct 2025 21:51:41 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfe221afc52131d890a73189fbc9db880c4db85efeea9c2b01f7b770362fb53`  
		Last Modified: Tue, 28 Oct 2025 21:51:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9f2740cfc5df08e6f26f0163fc5e5fc2122799c72cdfa8d579963e392e2b4`  
		Last Modified: Tue, 28 Oct 2025 22:12:49 GMT  
		Size: 12.2 MB (12177982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:c6eafed1110c9186dd84780531a73d632d9cd7e33ccfffc6b9494d676835f03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4286309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc3d47a679ac6ce6b2a39b1d3dfc97bc60a2a43396412a60acfaa8fa96cf959`

```dockerfile
```

-	Layers:
	-	`sha256:5ada03fef3d0d94616ac76acab2daf96af1e0053740deccc9862ae4e8dc90654`  
		Last Modified: Tue, 28 Oct 2025 23:52:36 GMT  
		Size: 4.3 MB (4262149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b84ce561a20fce834749c2c329b4af7ec734580459891ab9cc5740cb91121d`  
		Last Modified: Tue, 28 Oct 2025 23:52:37 GMT  
		Size: 24.2 KB (24160 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:5f963fb8734b6cf2af3761a032d9a4e0a12074b6242673e5b2d4fa2971b7de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76714505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849ff7dc392d5806ebb3630edec2adc50520db235bed1540d7c542bd7fd97560`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:00:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 22:00:48 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 22:00:48 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 22:00:48 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 28 Oct 2025 22:00:48 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 22:00:48 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 28 Oct 2025 22:00:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 22:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 22:00:49 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 22:00:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 22:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:11:28 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c90b06a6517c6ae94f592f365a7cfadf1534d1dc5bab4ac2c2e9592928a6cf6`  
		Last Modified: Tue, 28 Oct 2025 22:01:26 GMT  
		Size: 30.2 MB (30215463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f095a03f4dff18d1002e1e2ed9b748f88a5e4b78b69793c0c06b947d1f013ad`  
		Last Modified: Tue, 28 Oct 2025 22:01:21 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f3f8ae1eea1eda01496a572f08be76918005bc1aeb4065130e9b6c06ba6135`  
		Last Modified: Tue, 28 Oct 2025 22:01:22 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd3ed441c5ea3c1eb7280fe504a7f3f54e018c3ad0ccb7a95c68bc6db6da837`  
		Last Modified: Tue, 28 Oct 2025 22:01:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978056e2e01f0aed8a537de81980b602c61318be6d093a9bdc662a3923967216`  
		Last Modified: Tue, 28 Oct 2025 22:01:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed965d39272197ffdee5cb1a356591c87e886f2e53e68026a7c96d957179fd1`  
		Last Modified: Tue, 28 Oct 2025 22:01:22 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422feb684c60a60467fe4dbfde449cd6abce466cd9fc05590d1e4e84ef8655d3`  
		Last Modified: Tue, 28 Oct 2025 22:11:54 GMT  
		Size: 12.9 MB (12895927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:92a491f4c4c8b89bfab336b09b879cb7d79f7dcd0b3d5b4d56bd00b314a8edf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec905f7f27e1e9f67a2ad31fcbc0cbcaf910952e6f422535d091506e8275261`

```dockerfile
```

-	Layers:
	-	`sha256:fc0f042b1833ea69200a4d4fa652a7bfd05db3bc2804d32f7c65895179941fdd`  
		Last Modified: Tue, 28 Oct 2025 23:52:41 GMT  
		Size: 4.3 MB (4273369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86552df47bfab9fc83a60a84ab75af659f3b6d4938a31e27790d067c1aea85c`  
		Last Modified: Tue, 28 Oct 2025 23:52:42 GMT  
		Size: 24.3 KB (24302 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; riscv64

```console
$ docker pull nginx@sha256:b415bcad5367fbb2b17ef1466935a2e127395906a47dc2a8b385c8f3b22be79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66784148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5f6a322c8407dab9a4490ca4fb33cfc8f7ff1eab731a29eaef373146538cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cd6dcb86b4235073e4727dcec4dd102f680d4f6463ab9670294cab0254b310`  
		Last Modified: Tue, 21 Oct 2025 05:51:25 GMT  
		Size: 26.4 MB (26395250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde37d1704c65afb95f2e9ad8f53c73a10c8c4a93e54f149af76e0b78571ee5`  
		Last Modified: Tue, 21 Oct 2025 05:51:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9b72c256b234e9fa2c1aa6ad849bb0e889a853f6737ea5a72f864a570b1acc`  
		Last Modified: Tue, 21 Oct 2025 05:51:23 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fad4cf86f2a407820b0d138fd43c139d350a30339887e616b54bc29a601385`  
		Last Modified: Tue, 21 Oct 2025 05:51:23 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200d004fa9766d6b43b9fe06a7408cee5311afbad65c79bdb9288eb431c3464`  
		Last Modified: Tue, 21 Oct 2025 05:51:23 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d85dd73a2ea4e74c4b356ca6b6f83bd78fdc539a8277a23d789d8c8c1bfd10`  
		Last Modified: Tue, 21 Oct 2025 05:51:23 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e5f7d7c9100bc2292c34b17123165f7561023803db9959046f34e2fc909aa`  
		Last Modified: Fri, 24 Oct 2025 07:06:23 GMT  
		Size: 12.1 MB (12108643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:01c3e063b8589af29428a25f4a83d203662d8caabf0d036355c9940f34ed0246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd81c1e0c2fd644e3ea631b32ab67ac01351cb7c708e72c651b9878d6d76ea7`

```dockerfile
```

-	Layers:
	-	`sha256:291d9c8a55b7e4baaa62b35f3223bdbb1de5627e0c416b4e178924b452c287c1`  
		Last Modified: Fri, 24 Oct 2025 08:50:47 GMT  
		Size: 4.3 MB (4257569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33100b6cb5fe734d5aefb7d3630e6832ae90fb3587e9f38505cf9252392bbe56`  
		Last Modified: Fri, 24 Oct 2025 08:50:48 GMT  
		Size: 24.3 KB (24345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-perl` - linux; s390x

```console
$ docker pull nginx@sha256:39dcc806db66546af9a38235506169ed86822ecc7e7f07c9f28dc90b5dc3eb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70145325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78499f762615fac961516c029e46e10366800e0ef55575668eaf20e636d5b634`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b346632e6d8c457d097107c141b9854adb8a53c8975f50c7ef5f597a8fb5f13`  
		Last Modified: Tue, 21 Oct 2025 01:54:35 GMT  
		Size: 27.1 MB (27120512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96e323221004f97fef502ac328df0ac29c381daae44706f3392a91134b8d409`  
		Last Modified: Tue, 21 Oct 2025 01:54:34 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ae87a670a7df5ad51b81942da15cb1ae5b99aa6a709c6be86b432f35cb68e`  
		Last Modified: Tue, 21 Oct 2025 01:54:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d507dff1ae1932c79a8810161501023cc328d247dd27ed98734dfcaae5c38`  
		Last Modified: Tue, 21 Oct 2025 01:54:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1ad3850f60e8fce9f3b4d85de70ee23fdd3436897bd7a30a6fcd3d1f47cd57`  
		Last Modified: Tue, 21 Oct 2025 01:54:34 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eae0543514050586fcfe0d02b6b24a215221a3e867694a7d8eee679bcc0907`  
		Last Modified: Tue, 21 Oct 2025 01:54:34 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aefd80d636c70292e7d5ac611d72adb8674709c9752d37f10a93780c8d75751`  
		Last Modified: Tue, 21 Oct 2025 22:55:17 GMT  
		Size: 13.2 MB (13182961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:14ba79e0b28a7b36f697b509d3831d16a052c2af74fb21492f40f077e2615c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34368dc596f6215b8a217c0249401651243fd4542e50afd153e71e304ef3884e`

```dockerfile
```

-	Layers:
	-	`sha256:f5974053841a1c3f204283fa12cd3f339d9e21f1ab70e257cfc670a51f149af6`  
		Last Modified: Tue, 21 Oct 2025 23:50:51 GMT  
		Size: 4.2 MB (4175975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a013fe2fe36f38194dd0024b992c10f0e533ab55b11a129d6eef6aed5483a658`  
		Last Modified: Tue, 21 Oct 2025 23:50:52 GMT  
		Size: 24.3 KB (24266 bytes)  
		MIME: application/vnd.in-toto+json
