## `nginx:stable-otel`

```console
$ docker pull nginx@sha256:06f1eb4adc612033fe260feaadd8a86cf78eff309a92729c029b6bae6e1eecd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:stable-otel` - linux; amd64

```console
$ docker pull nginx@sha256:2456fe68e5bcd7995ec35031058731e5dadc352020ac30f96687f6a0ac399706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aab76f6db180d7c6fed3690d609a1758ef730e551cf611c5e3e2ab82e99cb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
# Wed, 23 Apr 2025 18:00:49 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ef3e0e5857820b7dd184d642837783b8d557826eb731226a9d1e63ad8b581`  
		Last Modified: Tue, 10 Jun 2025 23:28:57 GMT  
		Size: 44.2 MB (44150919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e4b92ad927e926ba1827b24aff9b20638e28117feae6495ec5c9dbbda2499`  
		Last Modified: Tue, 10 Jun 2025 23:28:54 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d04a5c77da84390a4e83cb92c112a0110df8d043bffda1538dc323962c5c2`  
		Last Modified: Tue, 10 Jun 2025 23:56:43 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d09fb06e13b7bafdb7a95646cb80cc48546c9c1a769291b32561c995735aab`  
		Last Modified: Tue, 10 Jun 2025 23:56:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03738b50bb67a99ac3c7727853c7cd549d2e86451add631429274324b4904`  
		Last Modified: Tue, 10 Jun 2025 23:56:43 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683f31b1c8fd84e0b2aa66c40be15e0a2f78b9b0876dddcd1971a7e903dd475`  
		Last Modified: Tue, 10 Jun 2025 23:56:43 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5381f8b67fbc05174b4da358dc60de0e0223a2d6c5b907ed13dc59a4cfae4b8`  
		Last Modified: Tue, 10 Jun 2025 23:57:11 GMT  
		Size: 3.5 MB (3520454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:50ffbb0a66da4d475f55151b225de56974f68d89156f949d9044947aa1e47885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae736c465ed191d8962b7f4455ea8f3d4a938ffaad8a95bef7edc2db5d7ab6aa`

```dockerfile
```

-	Layers:
	-	`sha256:6453648cd464483ead7f5519ad9fe4b0ee2598e89851c0b41ca54c887f8ebb94`  
		Last Modified: Wed, 11 Jun 2025 02:52:45 GMT  
		Size: 3.1 MB (3115996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000460ec73f3f65cfd8844f17a0bc411739e9e6f0988edc9049768a9b29e188c`  
		Last Modified: Wed, 11 Jun 2025 02:52:45 GMT  
		Size: 23.1 KB (23144 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7f87e25ae64c6356dd13c89b5866510fc33dfe2b79a6ed0bed8cacd51b4aad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72184675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed144f6865d2f499c75cd4f50658d1cd1e884075fb1c14a5361dd0e4db0099`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
# Wed, 23 Apr 2025 18:00:49 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3344b4d384131b49cde0abb048ec1693148980cee30619fb37f6c67ab19a700a`  
		Last Modified: Tue, 03 Jun 2025 13:35:30 GMT  
		Size: 40.8 MB (40755057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34234cc449f9de2a237fab2d55916dc3defa6b9509432cb3a6c930e35027c9d7`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d248d3ff83244304e9c25a9bf00520267f4ad07cc05292f13d028a0594e1469`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567c9642f4dc8cee60cd32205cd245a489876e966aae2a24c3214a855001526a`  
		Last Modified: Tue, 03 Jun 2025 13:32:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9474da7c59e49f888d96017979bf63d1fe175a93132291ddbc0ee203bb52731e`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e8ecdbfeef2dfcb2743daf4dd748fcbe2a4559e05272d278ece378f3fa204b`  
		Last Modified: Tue, 03 Jun 2025 13:32:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6070a9958414e880cf646bc2903bd17d090e2b66dd6cfe032161ba2c18e7447d`  
		Last Modified: Tue, 03 Jun 2025 15:12:03 GMT  
		Size: 3.4 MB (3359741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:4cfa52996001696fe7150b55d959e17d1cc12aa74453cacb11d8f63b23118357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a34ad45d1eac8c5e0a1f7a2a706f08c3619b88a1d86104e52de680342df57bb`

```dockerfile
```

-	Layers:
	-	`sha256:f2a1dc3775632dfed074ea617c2ce939ac70a672c76110d196f4902bb54d081f`  
		Last Modified: Tue, 03 Jun 2025 16:03:22 GMT  
		Size: 3.0 MB (2998177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a65e3de7622129754d1bebf5d1c4e2b0b11d09973a177755fd743314cf91a0c`  
		Last Modified: Tue, 03 Jun 2025 16:03:21 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json
