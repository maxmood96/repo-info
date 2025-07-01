## `nginx:mainline-otel`

```console
$ docker pull nginx@sha256:9d09b73dfd9a2e8de2849c1c89554d3520764c6806dff89b4c8b4487b73e9524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:mainline-otel` - linux; amd64

```console
$ docker pull nginx@sha256:ebe87f0215378de425c053a5a932610d866524f6873eba4c2ca83828bdd95e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75724710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2699106fc5fc2662cf7e8acbf222ca3f6a7a025478dd845d0af3ca3faf566c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Jun 2025 20:52:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NJS_VERSION=0.9.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 24 Jun 2025 20:52:14 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8e51cf00871b029c189d3e2145e2307bbba361bb62e20b696c18b2e8cd2f52`  
		Last Modified: Tue, 01 Jul 2025 02:13:14 GMT  
		Size: 44.0 MB (43969536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbbd7ee45b78c411208ea69e41a52a06a7e3872dfd0235e79bbb637e4789c1d`  
		Last Modified: Tue, 01 Jul 2025 02:13:10 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48670a58a68fc689138b916491d7c5aa6ea6fb2e4227a7edef275ec7003c9569`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7132063a5679c245d63b972b414a24de1686b42f8231c8df6f703c50a5ac38`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e05839d684c6d82bd5fd45968bb8997da3a639f1fe8ca502a4edbcffa8655d`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95256df0301df55618ec5c24f6bf41b6d005d3026e0e67e95fef0b0fbc2691`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fc09a83c670f21f9a67bd7362f2d9611b5f74148adfb5eefa368f5d35bcd88`  
		Last Modified: Tue, 01 Jul 2025 03:18:57 GMT  
		Size: 3.5 MB (3520438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:49dd21e16ea58a77b96d57b38dd45c06504bb381be6975e9a1201383b3b33c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f13de79bd1a0080901f672538bf7155c3fad5cb472f8cfd37c390ceb79d0e0f`

```dockerfile
```

-	Layers:
	-	`sha256:17c551d13e7bdb5548502421c0892e03ad07280e608746ee827ec0f146cf8bfd`  
		Last Modified: Tue, 01 Jul 2025 05:51:03 GMT  
		Size: 3.1 MB (3118606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a3732f19dd27ea72279e2203c108a5c01bfe81fcc125d1c94c60da253a72e4`  
		Last Modified: Tue, 01 Jul 2025 05:51:03 GMT  
		Size: 24.4 KB (24388 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:da2405dad0ae71648b4443913e440a6887bd789e4df17e2036c5d2c60327ce60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72086801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3f0e2bb4fe345a5170244c00e5928d4f79b7a84c8c3fea112767e2ed07bad9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 24 Jun 2025 20:52:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NJS_VERSION=0.9.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 24 Jun 2025 20:52:14 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b122e31aa620a55313a4295ef5d368a83d9fca362793ffd9ad2067652d523e`  
		Last Modified: Tue, 01 Jul 2025 03:11:19 GMT  
		Size: 40.6 MB (40638505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004c60765aadf4911eca468cd5cd1f717783c40c74d817f825113cb2f0adc0ee`  
		Last Modified: Tue, 01 Jul 2025 03:11:17 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7243db3466b30350df79fd507b1052fa6ee81aa60b8fc0f094170b9323c1cdfc`  
		Last Modified: Tue, 01 Jul 2025 03:11:17 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1184df424fa0de9f9476f9ac7cafaf604835250e57f90dcf38c568cc52dac7c1`  
		Last Modified: Tue, 01 Jul 2025 03:11:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7482a68d7c6477f9f7b0c81dbf107e1ad8e3ecbe2130600dbec80b381eae0460`  
		Last Modified: Tue, 01 Jul 2025 03:11:17 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac604e5e41f4e769444975b5109c2842d417d7e254550c82e69835c511cbe91`  
		Last Modified: Tue, 01 Jul 2025 03:11:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d346bbf2da1b4c10a1b8b2b99e74f43c366b8ff84f5752fc75bd07f9575fb936`  
		Last Modified: Tue, 01 Jul 2025 13:01:03 GMT  
		Size: 3.4 MB (3366024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:13044de74af1d1139635e6a853b4057ae28b11017d025013111827cb286ee9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3032d6e7cba562a8b7967e978cc66b5926fc383a7e87501a78d13454663097`

```dockerfile
```

-	Layers:
	-	`sha256:60f621ad2c675a6730a403a2d684a4be036c6573655785bb61a3254eb3685d9e`  
		Last Modified: Tue, 01 Jul 2025 14:50:36 GMT  
		Size: 3.1 MB (3119058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f2437331dbae2dc03bf94043a02973eb14774a084b52e9794e1a3ed3ae6cee`  
		Last Modified: Tue, 01 Jul 2025 14:50:36 GMT  
		Size: 24.6 KB (24565 bytes)  
		MIME: application/vnd.in-toto+json
