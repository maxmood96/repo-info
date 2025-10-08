## `nginx:mainline-trixie-otel`

```console
$ docker pull nginx@sha256:4f40f45115822b5bf797e54e5ca779841e50408ab548f28ebb322f86daaf6a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:mainline-trixie-otel` - linux; amd64

```console
$ docker pull nginx@sha256:d0f2fa0a003fac83b758d726cbf8c0aa1e1ac04b8560b50d3bb2143464f76d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66395561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf905b68d82cefcbb096912ac0cef897852f3b36dd07ccd201158b22686987`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b90fb2b9a5a65efddd2ffe8f3b24b04b8463f43c69b759cbb85b72329380b`  
		Last Modified: Wed, 08 Oct 2025 00:14:26 GMT  
		Size: 32.9 MB (32902769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ea9f4c626de724115534b787f32f091b5f5e41668a4a33a385466e8e3e185`  
		Last Modified: Wed, 08 Oct 2025 00:14:23 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d144c4badd75d84d5fcf15ff49774be2abf4e24d7d3e3d2311916213d59496`  
		Last Modified: Wed, 08 Oct 2025 00:14:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b459da543435bf9437ad7530b6c62d7d40b9e8d84b91945cb0443d4a14664ca2`  
		Last Modified: Wed, 08 Oct 2025 00:14:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da8ed3552af163aaabf15e69703265c1770edbe15bc4cad5cbfcfa0ac943109`  
		Last Modified: Wed, 08 Oct 2025 00:14:24 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e822d8ee0c638c33ce3efb93b0913fef8107da4436a7116b986ef44c281182`  
		Last Modified: Wed, 08 Oct 2025 00:14:24 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d3d6667f844bc77b6a7b84b2eb17b02a8d2a221a9f2c728b737f96c19b40a`  
		Last Modified: Wed, 08 Oct 2025 01:11:06 GMT  
		Size: 3.7 MB (3710425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:72bc128d942bd032732d11dea9e129473d7418dd8e27b0efa05cd99ad5f447d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c7be9fbdb91812cf06f212ab457dd4b01f5f7c62787f1134752a4153aa1bc5`

```dockerfile
```

-	Layers:
	-	`sha256:5d2bdfc3dad665b57ec2d435a86be0ee8fa4493ce6a87057473ceb9185e9ee8f`  
		Last Modified: Wed, 08 Oct 2025 02:51:56 GMT  
		Size: 2.8 MB (2823330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ef26d88c11b635cc716d25e18da1e45b4245f6d46d2b8dce536ffdde1a7ca6`  
		Last Modified: Wed, 08 Oct 2025 02:51:57 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:6aca220639a3b0097cad82d7993ca25941cb515a19ec4b67ada8c29fe913fff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65025131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cedbbbc488fda5d4ddf9fd0d087130f94d7059699e7404a4ab5732ff5e3232`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ff5b8e6ceeed5bedcc0392eec8e2a179345273f1c959e09b7dccb5e00aeda1`  
		Last Modified: Wed, 08 Oct 2025 00:14:19 GMT  
		Size: 31.4 MB (31410297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd736256ac638f208ebb336a9d81cecd75c72149c6ac3c7fe77fad02864d49a`  
		Last Modified: Wed, 08 Oct 2025 00:14:16 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348644581cc5d24965bfc046dce878d56b342fa8350546085301513cf822dc26`  
		Last Modified: Wed, 08 Oct 2025 00:14:16 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e8c796c790b689e2bd0806c36ec6aa58964b2cc5f8f0fb69da3e21339a6b83`  
		Last Modified: Wed, 08 Oct 2025 00:14:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54959f07be7fd631a94375c1d36c8f3e3b1b653f951fca13ddd80eff18cdf57c`  
		Last Modified: Wed, 08 Oct 2025 00:14:16 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3766556f33954926819141a6eb137efdd45cd158ac13bf576d561889defd87e3`  
		Last Modified: Wed, 08 Oct 2025 00:14:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d077e0f028ea42fdbbc4b6cbfb7d19f1bb6c668e7167de7372c36acfd1fc20fa`  
		Last Modified: Wed, 08 Oct 2025 01:11:03 GMT  
		Size: 3.5 MB (3469395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:4cc2bfc34ae54b21e4f6668fab16da6af41f5a9cd78768240f90120046e6b4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6baade125ba7d775a9970f4b3df9901967e31797a02b825196fe3fa2f2fb5bc`

```dockerfile
```

-	Layers:
	-	`sha256:e80c2af3a28e5b2c95e1eefe4db11d9e1b8ee82a52182ce168ed5d2d2e174432`  
		Last Modified: Wed, 08 Oct 2025 02:52:01 GMT  
		Size: 2.8 MB (2823815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550a47847f0cfecbccd220b2cdf0e85151d6b68d7d21076d26fe60446d728de3`  
		Last Modified: Wed, 08 Oct 2025 02:52:02 GMT  
		Size: 24.5 KB (24537 bytes)  
		MIME: application/vnd.in-toto+json
