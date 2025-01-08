## `nginx:1-otel`

```console
$ docker pull nginx@sha256:7a0c99a7d95768c2c51d4f31ffb01cc240be76aecb6fe190513973f772ea648a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-otel` - linux; amd64

```console
$ docker pull nginx@sha256:c80edb0dec6ac163b81f1c2a1fc7c1d640c8683cb846865d1ea2bed5a5b85d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75060022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f326e29cc566253c4356480fb713cbc5a72febaf69c053e907ca3018753fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 26 Nov 2024 18:42:08 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566e42bcee1cd697dcab6098c082789af33bc8cbcbaa95c8adbad87283c85c75`  
		Last Modified: Tue, 24 Dec 2024 22:18:06 GMT  
		Size: 43.8 MB (43842081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b99b9c5d9e5679c839357944d083c55c4c045e2cae21f84dfcfe5841e2ea59b`  
		Last Modified: Tue, 24 Dec 2024 22:18:06 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd98674871f548eff8a4e4f3d4aa1ba504320ccbabfb0a217c4ea5c23b6144fd`  
		Last Modified: Tue, 24 Dec 2024 22:18:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e109dd2a0d75eb2ab2491daec5b300e99027ffdd528998612b693f3347b97e4`  
		Last Modified: Wed, 08 Jan 2025 07:47:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8cc133ff821c8b0ac7a6667e3a2e70ee6eb04f850e38088f59720017a869db`  
		Last Modified: Tue, 24 Dec 2024 22:18:06 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f27309ea1a5e557aff07fbd5ece457d5cb85583f795b34f342d5550a08a5c`  
		Last Modified: Tue, 24 Dec 2024 22:18:06 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7074aeb53a953da7c8d2c05616f26a6987be929128a4b91eb56929af07cbc0b`  
		Last Modified: Tue, 24 Dec 2024 23:15:38 GMT  
		Size: 3.0 MB (2981761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:8538aa9f629bfecc38d751186e0c767b191158b878493220aa57970b5596bbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd0be59cfb3e2c58d59c95ee4cc45e4225de498118bcee00892910c87a57050`

```dockerfile
```

-	Layers:
	-	`sha256:db20ef082b793a9e0a945000f80d8440ea73dd203898bc6db4db9e917a9ff4ea`  
		Last Modified: Tue, 24 Dec 2024 23:15:38 GMT  
		Size: 3.0 MB (2965629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa05f7802dc112a3e17a3a779a5e2013af149ae39ae93067f6924099855060a`  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:01146d79a2e4cc5f60b28dde2ad3193abed8b314b54a5f9923bd104cbc303bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71348712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a86029a61f5e7370e049b5ed1b3acb061ee332eec05daa8c8f71cfb3eec3bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 26 Nov 2024 18:42:08 GMT
ENV OTEL_VERSION=0.1.0
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb964b66a74fdd475a8375186208cf5197c3189e9a01b3311a3def1d6d787ce`  
		Last Modified: Tue, 24 Dec 2024 23:03:01 GMT  
		Size: 40.4 MB (40440317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5368be906ecbd8443efcbfac77af24ab15e33c8fa95acff4dfd2dfeb7cc5ef7`  
		Last Modified: Tue, 24 Dec 2024 23:02:59 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755bf136756eefb75d93c3f29a903375d95198c05d08fa38d288a5572835aac3`  
		Last Modified: Tue, 24 Dec 2024 23:02:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc2e219c2002b8eff3c5d3bca849ee157e5d61cf52ec2fc31b2814d99fa291`  
		Last Modified: Tue, 24 Dec 2024 23:02:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c6a94b398bd46eee583da22742a4b92e207fa4d8512f3988d873898599b74`  
		Last Modified: Tue, 24 Dec 2024 23:03:00 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8066ea4829bb718d6a47f0b4e84822fd75feedce825f9694a0305dea15ef5fc`  
		Last Modified: Tue, 24 Dec 2024 23:03:00 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4358057f51dbdc80fa8ed0f1fb3c49120b6d12fb26cd1a4d01e4d7d921f0064e`  
		Last Modified: Wed, 25 Dec 2024 07:48:45 GMT  
		Size: 2.8 MB (2845071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:96e03529f2caeefe2635c2181bedbe08c32608d806a36ead7006e066dd463362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6584ead2a016bdf29c894a7deb9837a4f1b03f771e8aa82fcb5d63c760c3736`

```dockerfile
```

-	Layers:
	-	`sha256:779a081a47a3028476e53503fe806aa6999c929a7ba2a4d0b68be517d3813114`  
		Last Modified: Wed, 25 Dec 2024 07:48:46 GMT  
		Size: 3.0 MB (2966081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389a28736008924efa30d01ba0c865b034dfe8866b9af2979a7d9e682c90e16f`  
		Last Modified: Wed, 25 Dec 2024 07:48:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json
