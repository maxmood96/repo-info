## `nginx:mainline-trixie-otel`

```console
$ docker pull nginx@sha256:84bcd77e3a3e4b0fb8bc58eb62dbd76715be2ff107fb01d3a5dad5b71a8842d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:mainline-trixie-otel` - linux; amd64

```console
$ docker pull nginx@sha256:4d9dcddf1c2109b48113145e65a5876d448cbd77e8a2e3ead04e6ec27e2e8b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63486551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4fb8bd1483a1b8141f878d335779498534ca6effc3344e37299850add8f20e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:22:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:22:19 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:22:19 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:22:19 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:19 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:19 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:22:19 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:22:19 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 01:15:00 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 30 Dec 2025 01:15:00 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcea87ab9c4af08933def1f0ca20657cd60a28e8821acd12f28c47dbe7c44ce7`  
		Last Modified: Mon, 29 Dec 2025 23:22:35 GMT  
		Size: 30.0 MB (29994846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35df28ad102658dd2661f97d891342916a766b37d638ef196d7e10f953065fc7`  
		Last Modified: Mon, 29 Dec 2025 23:22:33 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ae2d6d05ef5203709c239051994c6b2ee90747b8adc2c883544c6dc0064d8a`  
		Last Modified: Mon, 29 Dec 2025 23:22:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b00848867934ffcbfa9616c7270be78dcc53f9c932c90755a5467a8af75d84`  
		Last Modified: Mon, 29 Dec 2025 23:22:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ca78f31febb8f2ba285ba9c2547eb66dbbbc8cc3f8bd76305d67fbafcbe9b`  
		Last Modified: Mon, 29 Dec 2025 23:22:33 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6799cf0ce70324edaafce41cf70d3483ec2104742f5657bf75729081110cc32`  
		Last Modified: Mon, 29 Dec 2025 23:22:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e7c99f9b9654d5a2ec25086118a9c67589a8a9472838cf7a8d33721e583735`  
		Last Modified: Tue, 30 Dec 2025 01:15:14 GMT  
		Size: 3.7 MB (3710576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:eb9f5089f5dd10ea93c8ffb950395499a10588c5c722e18b121e6287981d269c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413e43ff1cad2fc84da7a78fdc45787d00a0acedf6c14872e6d14efedce7b653`

```dockerfile
```

-	Layers:
	-	`sha256:9c838418259b359e3347c78415e9ba098d557a3f3685b331c90d22c673029f64`  
		Last Modified: Tue, 30 Dec 2025 03:51:07 GMT  
		Size: 2.8 MB (2823468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e123a9c3a46f02b1c83d753c5980157f110de7fcdcbbafc081f748534f71d0`  
		Last Modified: Tue, 30 Dec 2025 03:51:08 GMT  
		Size: 24.3 KB (24318 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:6777481bcfab5f8debeee57af92f6d104df654ec01b0d767a46d21516b313ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61733173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c34974e920243312d7d13c16abdb850a0c8711a3b76e6007dee41dbec68dd85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:22:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:22:17 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:22:17 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:22:17 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:17 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:17 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:17 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:22:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:22:17 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 01:16:31 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 30 Dec 2025 01:16:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3b30ae197fd143213952b17dc03e0209fce7dfb4f306d00e01501ac6e92a1a`  
		Last Modified: Mon, 29 Dec 2025 23:22:39 GMT  
		Size: 28.1 MB (28120415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3276fb849f5952c72d1e94b9b367ba70d554e497c8fa121dc92978377c35c4c5`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f02391f1636526164275a5e5aa7e34e86685e17e97158468c9765a26ef21ee`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6c73a28c57a4b0a454743868191f6d90154cbdfa00c3a590983ca8058a9d97`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac08499d0aaf863c61fd0f1e7b867c62026cbd3973f8bed40bbd2cb797fe42f`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e794dd6ce7eac9245e7e73789e38e97277997005bc849a6742a2c7cef85b10b`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3133e7554f0e907c7029d4562acf4199dc6e45089f16c015193187d05abdd68e`  
		Last Modified: Tue, 30 Dec 2025 01:16:45 GMT  
		Size: 3.5 MB (3469529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:05f499e3577c63244f69a55848f31b0a563fc809afe276c13ea0defc2f8cbf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a918c5812c2e53a3a3e6d2a68dbe82c274b355ccd52c2be6441f656ac277fe`

```dockerfile
```

-	Layers:
	-	`sha256:39cc06ca83c7a995c68befcc8f64bfc426c1422584fbafc6fb3a2c4d88f4c7d1`  
		Last Modified: Tue, 30 Dec 2025 03:51:12 GMT  
		Size: 2.8 MB (2823953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0066e5e20e1d4492a0b4a7cd411e48333b497a3f3250ffe8a8d9e670eec2470f`  
		Last Modified: Tue, 30 Dec 2025 03:51:13 GMT  
		Size: 24.5 KB (24494 bytes)  
		MIME: application/vnd.in-toto+json
