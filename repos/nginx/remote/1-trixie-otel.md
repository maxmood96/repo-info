## `nginx:1-trixie-otel`

```console
$ docker pull nginx@sha256:d8ffda20e0c5223a2802b9984f7a066d7e40d9e28621a27e6bbaeb974be03822
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-trixie-otel` - linux; amd64

```console
$ docker pull nginx@sha256:0b48e5e15c6961f82bac0ad33da213b7d0b9da3dc8d4d1da74c483bb4c88465e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75a5b3165ae45fc1e306121be40e4497b2cacb6fc23d9bd6e307244134c31cc`
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
# Tue, 28 Oct 2025 22:10:45 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 28 Oct 2025 22:10:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:03cc03ce9151fb3b85b0daed4c87423c2b848470b9a705ab732b9cdb523ee80c`  
		Last Modified: Tue, 28 Oct 2025 22:11:05 GMT  
		Size: 3.7 MB (3710254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:06e2ee93bd3c81cfffbd0cde8653b8554af738e47c93dd68bb1646c05ec0adcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4bf9fbdbd5df97a5ffca3a28c66a7118e70762f322d9c27a0493dbec4b226b`

```dockerfile
```

-	Layers:
	-	`sha256:922b9a8c81488caace9a77cd2fab2aedd475a189b24e4cdde694d7f80b1f6982`  
		Last Modified: Tue, 28 Oct 2025 23:52:01 GMT  
		Size: 2.8 MB (2823366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9290de5d8d4f6aaf7fccc12db7c017da6932256914fc6d8e9062598c9f367070`  
		Last Modified: Tue, 28 Oct 2025 23:52:02 GMT  
		Size: 24.3 KB (24318 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:1a8d7b04f1a7ee41ef6e1c6e62dc19beae8a9ba98642bc5b0f23a55744dbbf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61705123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f3e6b5aa1411b4ccfefabd4d598e5e0cdec856ea1fc70cd3ae68d5621e5f72`
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
ENV OTEL_VERSION=0.1.2
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:5c79af2ecde9253c3cacd79f5c5c058780ef191de6c86aa2bcbec52ac3143458`  
		Last Modified: Tue, 21 Oct 2025 02:31:57 GMT  
		Size: 3.5 MB (3468839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:754db73ef59dc78bb01d3162d435fc5429bed8b5274ee008ad92c8828c7c4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe0eb2e931492514feb03b6131e14e28118dfd24a822f7895fad4c679680c7d`

```dockerfile
```

-	Layers:
	-	`sha256:c782f5ff3369f281c1c49bf66b62b97d67874950b2dc70748445bd2a0d55b4b4`  
		Last Modified: Tue, 21 Oct 2025 08:51:04 GMT  
		Size: 2.8 MB (2823851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad9f1b2573b72cb49488c23f309fffb014572f35ab1e26cec90188e58f7dda7`  
		Last Modified: Tue, 21 Oct 2025 08:51:04 GMT  
		Size: 24.5 KB (24536 bytes)  
		MIME: application/vnd.in-toto+json
