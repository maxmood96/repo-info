## `nginx:bookworm-otel`

```console
$ docker pull nginx@sha256:370485c02a0796983291ced0e51a3fe93c7f50157c72f950e79b0313b457d231
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:bookworm-otel` - linux; amd64

```console
$ docker pull nginx@sha256:b586a92184d7d659cd30f85105f651a8dbaaabb03821c61c5934339db862ba22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75824548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02c180c88450f18cce8e193c2fc706feeb42d300b85b38a3031f6c56a13dd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NJS_VERSION=0.9.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 13 Aug 2025 16:34:01 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375a694db7346a00da49aac62757cec58667d0c90874d4b08edef1814161f8f2`  
		Last Modified: Mon, 29 Sep 2025 23:56:12 GMT  
		Size: 44.1 MB (44065216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f825f15e2e0140c77e43d026664718f274284e907b3dbfea8af5c3f2e843673`  
		Last Modified: Mon, 29 Sep 2025 23:56:06 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d05858bb8d98a948d273ef83ff992f7eb4b7b50b9d92dcb186ec02d6cd1089`  
		Last Modified: Mon, 29 Sep 2025 23:56:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cfef42fd24116711bc1e323e83d40e6145937250f876e0342c2c90426c3bfb`  
		Last Modified: Mon, 29 Sep 2025 23:56:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc5fdd1317a723bde90305759b954dda6335ade70354d860e82c59588df4e4b`  
		Last Modified: Mon, 29 Sep 2025 23:56:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4e50e2076584d483a45b2db7718a03e941045e8dcd0023b6d326b743b282a1`  
		Last Modified: Mon, 29 Sep 2025 23:56:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988dacf26f9922e6f66d74e8eaacc9cf39ddbb4159db801461693b6e92bcd54a`  
		Last Modified: Tue, 30 Sep 2025 03:10:35 GMT  
		Size: 3.5 MB (3526399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:b7bc8300ea76243adc9219f3c2645fb731328f5385dc2057909e35fb1a6431d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4553be57561a5cbdc0d960a35924e219b9f08e89725d96f2f03472af16763312`

```dockerfile
```

-	Layers:
	-	`sha256:e502e2cd190c9cdf030760bb6e94114dc1c1ffea42f37fbce27eeb1b3f9cf049`  
		Last Modified: Wed, 01 Oct 2025 14:50:30 GMT  
		Size: 3.1 MB (3120721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c8f66db7b4eb766c3044eac73e7c65eb142b4968382c3e60b97ddfaffd8abf`  
		Last Modified: Wed, 01 Oct 2025 14:50:31 GMT  
		Size: 24.4 KB (24388 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:ade55d0acf687bf16ef608d0dcba4cc6e11633b9443ca4a69b6f4650175c3d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76ea880fab12c67998217a51e948eba681afabf2d7040bd5bcd96aefca54127`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NJS_VERSION=0.9.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 13 Aug 2025 16:34:01 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a2ff429ed911917cc7541492e92b083056c251a396562117f3259ea24ce388`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 40.7 MB (40741327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dff34614b43f1e7186ffe85a6de5af902a09c2231b06855a75314dbebb582`  
		Last Modified: Mon, 29 Sep 2025 23:56:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0838cc8bade63262b7ec7e9540ecd55f5f254e0bac6020f3362a811fa90bbf3`  
		Last Modified: Mon, 29 Sep 2025 23:56:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2e7b5dc9bcdbfb0e8119c35fd33fb8580c93813561ebcdea708b98e82f42c7`  
		Last Modified: Mon, 29 Sep 2025 23:56:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b278be6f74e8daedcf9071f2b01c74ea2ebed0d2b4e0a0d87f63365fadffdf`  
		Last Modified: Mon, 29 Sep 2025 23:56:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f648e62e9ca7ad38d7eedfda371f0237f5114f7ad9998c3f1179a8ea7cec1ba`  
		Last Modified: Mon, 29 Sep 2025 23:56:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac84e8e689693a8b5c61a7cb9d63060b8912ab5a18f8b09f654f1877359d59c`  
		Last Modified: Tue, 30 Sep 2025 00:58:05 GMT  
		Size: 3.4 MB (3372625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:cbe9567eef6cba99403c31c54cd7b6eaa8c17446fed99bbbb1bbf17498b71b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4cbd716158d05a8447742dcb950dc0f3bb5cecbeab7295d690840b1e01afb`

```dockerfile
```

-	Layers:
	-	`sha256:ed61f56b19859261cf70f2391fa251ee84940045f8dc12f3fe1e830cb8f4d6e3`  
		Last Modified: Wed, 01 Oct 2025 11:51:41 GMT  
		Size: 3.1 MB (3121173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a22de5b2c43663a88ab42212ed31934929c6cfb420bbaa12cab1ab703a6d91`  
		Last Modified: Wed, 01 Oct 2025 11:51:41 GMT  
		Size: 24.6 KB (24565 bytes)  
		MIME: application/vnd.in-toto+json
