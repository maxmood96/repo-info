## `nginx:trixie-perl`

```console
$ docker pull nginx@sha256:dc215d91cee08cfd17b4293eeba2304821593a9236e771c466b3c32102975f6f
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

### `nginx:trixie-perl` - linux; amd64

```console
$ docker pull nginx@sha256:60cff69e22089c1070ec9b156222061510caf09842f692036ae399bf2cac2cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75102675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c7cc14440159815e5f54642db3ccba3d3afe5828dfd38ad11f10c15acd0dea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:22:39 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:22:39 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:22:39 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:22:39 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:22:39 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:22:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:22:39 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 08 May 2026 20:22:45 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a7e44929f3a02caf5d606403b9c7f843cf5fd963a30bd77d9a4deea44cc4e0`  
		Last Modified: Fri, 08 May 2026 19:22:50 GMT  
		Size: 33.2 MB (33157664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f32fdbd611e27f05fbb3d972c3cbd1d9ce01dcf9743667b551f37a12b9d7a`  
		Last Modified: Fri, 08 May 2026 19:22:48 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a36159731b6c4f15992b4542ad824d7a1d3dee549d696ec8d4af8f0718466`  
		Last Modified: Fri, 08 May 2026 19:22:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d41cd6829d6a76246d76ad30405271259064cd1465c2f49b8f0f03a63675f5`  
		Last Modified: Fri, 08 May 2026 19:22:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83742381311ab223ac476c81482f79c2fd5f8cade0fdd7c3ee92574649e9ace7`  
		Last Modified: Fri, 08 May 2026 19:22:49 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b53b630dedfac569c0b3484f367dd8bdaa437b2dcff5c453b742fcba600cf`  
		Last Modified: Fri, 08 May 2026 19:22:50 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f90ebc1a012f0262d1dc7b09aa78ebe97a91bf9443147825099765bebccbdd4`  
		Last Modified: Fri, 08 May 2026 20:22:56 GMT  
		Size: 12.2 MB (12160189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:b89bf47ea2eaa26337033257a079bd5f6c51f45d1d74b08612b6fa2714b9d757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4265175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911d9f3fab0d2cdf44f4b5e6d31b5d66131531ad9635d9d27ca87dca8bc4b55`

```dockerfile
```

-	Layers:
	-	`sha256:d97f000b078fe283ecd779fd0f60f4652d41c7597563c92ce5f561021f2842a9`  
		Last Modified: Fri, 08 May 2026 20:22:55 GMT  
		Size: 4.2 MB (4240717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd27c635c8fbfb1bb2f4545c07bb16fec1757a0b5b33db2bac54c683f13bb0be`  
		Last Modified: Fri, 08 May 2026 20:22:55 GMT  
		Size: 24.5 KB (24458 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:9b1d9930527f87b434d02b897e4181c11d2cfe39cc4cfad117bdd72d03fe1b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66098358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff99732863c076bd6307b60816d327f36983d4ea72b39dbc66691ba347ece6bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 20:35:51 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 20:35:51 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 20:35:51 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 20:35:51 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:35:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:35:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:35:51 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 08 May 2026 21:52:40 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248401f980342939fee4bdb4ca9fb00391cc1aa9f64bd3563b47b38ad3f78c5b`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 26.2 MB (26199553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc941638861d65831d90b9caf1b2c9d1315947ff2e923fbe375ac4184521135`  
		Last Modified: Fri, 08 May 2026 20:35:59 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec5ae31c39e063380c2963694757fa05e0f3dace00508ff27ef9c00b918901a`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d671da6a4cdd2e80fc9fd343e2cd233f549217050b939eb93fcb5209774a09`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098863e501eb5764fa816da952454ce0e1102200cf503439e13575466e405d8`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e03ff89f4d7bd993ae573f1f4226d1ec56e334400d63bc6d2569506736eb4c`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16927bf6cfb746fac22c907bc48da0f3f0059e89b2aaa082a8953d4b0b4628d5`  
		Last Modified: Fri, 08 May 2026 21:52:49 GMT  
		Size: 11.9 MB (11946008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:7d1d5b6f600c1588206b30d898f8301fa98cd42d3d27148bdde5b39a226934fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84556de4068f5c77f0bed097abd41d1d6c57f2640025643ee7d77a8e203a1dd6`

```dockerfile
```

-	Layers:
	-	`sha256:51c9a6673e0b9859b45ebd13e4e27a760862903b248c057635feb2781796d8fe`  
		Last Modified: Fri, 08 May 2026 21:52:49 GMT  
		Size: 4.3 MB (4272774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1438a7cf34327ae6f0406365c5ec5506d9790afcfcb5b7e37f677f015f237021`  
		Last Modified: Fri, 08 May 2026 21:52:49 GMT  
		Size: 24.6 KB (24586 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:e43dd4af136d084e503a431be7a2e0ba684bb8067ca6e31c1650054b83a0e34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64117511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518303c821074b17265f555fa11808e56eef08ea4d693706a1496844e4afcf6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:24:26 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:24:26 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:24:26 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:24:26 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:26 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:24:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:24:26 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 08 May 2026 21:30:47 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c12dea6b68e914ece1edc0cb20c87b4489c8a716f3e354e2c95696c5631aa`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 26.1 MB (26141751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e814b586bf73d67e3579baf6c1080fdb4f8000ea859be552ea90c5831fed0ef`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6651b6ff0d24cd91e484161816d722d9ef78473d20aa6d0e0a04f2562e138afe`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc0c33d585f0caca673715dcc76092bf0b01c98a01ab46e3db5b7d1f0bdcc37`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490978ee28bd10e13b66791c5b29fd1c656598bca3bc5e9b9b356b9788638f0`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b383a10d7f7c8a8cfb7f750cea6ae2b04c9a148427193ed52ee51b24574cd8cd`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84591ba07c707d3ceed9f9030049268a3f24056939811b0eb08af28597e75709`  
		Last Modified: Fri, 08 May 2026 21:30:57 GMT  
		Size: 11.8 MB (11756248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:dca96a16abe0c7e0f342510a372648dd1cedec4a82c5055940e952c742fa8d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c732b7300380ef5ed4b87511f274b814d9094252e42e567da3eeb81c5b8bac6e`

```dockerfile
```

-	Layers:
	-	`sha256:1d0888c159bab01128235f43b1dccef213a83eafd721f60ce1e6b58c937a5334`  
		Last Modified: Fri, 08 May 2026 21:30:56 GMT  
		Size: 4.3 MB (4272295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d58ddd4978a60502682092728339e723bcddd2e482a3712eed95e1c7efb018`  
		Last Modified: Fri, 08 May 2026 21:30:56 GMT  
		Size: 24.6 KB (24586 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:97306d459d21b2bdde660ac59dfa0fa1355b28bfd8abb262901990071246c99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73393621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07da95b7bed476615913ccf3e88d380a64116b6e9504545fba78ca2f2a3fc6f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:21:36 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:21:36 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:21:36 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:21:36 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:36 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:21:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:21:36 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 08 May 2026 20:27:23 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb36225b641a6965b680bcd401a43615e52a42e93908d0faf2388cb088d143`  
		Last Modified: Fri, 08 May 2026 19:21:46 GMT  
		Size: 31.1 MB (31140455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233902120245103cf1634f36441eb74882a602b9c7934f85696d7896c8802aa`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e26c83bf44f3bf345dc97aed90b8a0cd2111861f2c76c35c29985c26a0b6483`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d472f762a89436d52a3327293fdc6b426321be07ffee13227faac78b82b466`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08d37673839087af78b752a824ef4f692acd5190a9eb34b91b8f6e4875d9c4f`  
		Last Modified: Fri, 08 May 2026 19:21:46 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d207385a9f9125e7d6d972d71854facba065523c9fe2b8d350264acb05e5a03`  
		Last Modified: Fri, 08 May 2026 19:21:47 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda8140ec25e90fa467ee6929934472b91fc9290605ea4b3706b4234e6f7f814`  
		Last Modified: Fri, 08 May 2026 20:27:33 GMT  
		Size: 12.1 MB (12104932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:6704a7d2d607cf95069da2b4c712530dd89c456ba168df323df263c48ff0d7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07cae4300cb4489d9ca55bec78fb686fba0142cb30f99d774d18ba6f2850de8`

```dockerfile
```

-	Layers:
	-	`sha256:88aef7b00895ae8145221638518131ebc1630ccdc22919a4a8bea14684fc569f`  
		Last Modified: Fri, 08 May 2026 20:27:33 GMT  
		Size: 4.2 MB (4247243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbdd9b87ae8c31cc61e67ab065b4b5340370cd2a5b56442ad8e7c14c72da465`  
		Last Modified: Fri, 08 May 2026 20:27:32 GMT  
		Size: 24.6 KB (24634 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; 386

```console
$ docker pull nginx@sha256:4afad5ed231d07f78a96dc19a59e355b1848a5eb285bebd125b5e15656430b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75509354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd91d05cfbd45ab375856838bf9fe5ee6992a6acdfc980db0e0e84a1eea48bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:58 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Apr 2026 01:23:58 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 22 Apr 2026 01:23:58 GMT
ENV NJS_VERSION=0.9.6
# Wed, 22 Apr 2026 01:23:58 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:23:58 GMT
ENV ACME_VERSION=0.3.1
# Wed, 22 Apr 2026 01:23:58 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:23:58 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:23:58 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:23:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:23:58 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:23:58 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 22 Apr 2026 04:56:55 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa64b825dc6a1bd010cc6d39e7bde7c4315ed5078c96215bc6b036c612f6032`  
		Last Modified: Wed, 22 Apr 2026 01:24:08 GMT  
		Size: 32.0 MB (32026611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2c9bca772377fbc1e94a34d2d797662ea01265ceb47a6229f6587ccb9f83a9`  
		Last Modified: Wed, 22 Apr 2026 01:24:07 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3159aa7dfd0c6bff6429c8dca784493e16608c890ad9d10e36c20a193a8706`  
		Last Modified: Wed, 22 Apr 2026 01:24:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a22276a816a97c05ceb52a3ff023d39dd2a70dfbbfba380335268f62ea8bec`  
		Last Modified: Wed, 22 Apr 2026 01:24:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0f8ff5bbd05372803331cb31f43f073b3718b230ca2e001e20ed4877c7524`  
		Last Modified: Wed, 22 Apr 2026 01:24:08 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8c08f721d44b0f89ed8cd081c8b4e87d4d24bfa2d2b4fb60e9f314c6a1bf7`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890f5ba1baf1f1a4efb2a3a5437e724770ea30862784f310718aa6a52668bcc9`  
		Last Modified: Wed, 22 Apr 2026 04:57:03 GMT  
		Size: 12.2 MB (12181826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:ae5d04d2836146aab9dafde91599fdeecfe3afa57a37ae26c0c819b72cbaa0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4292127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49cd508d11cb36a4ee219401a8befb6b3cef6710e6e4cb6020afe64a80fb1bd`

```dockerfile
```

-	Layers:
	-	`sha256:9e74747c4e8f851350ed3c735ff52568a4b9e5be277943bb5114dfca9d74527b`  
		Last Modified: Wed, 22 Apr 2026 04:57:03 GMT  
		Size: 4.3 MB (4267731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c38ea2a58a10316680c779a9e44107223d881767af627ad34b029f6c4e82fe9`  
		Last Modified: Wed, 22 Apr 2026 04:57:02 GMT  
		Size: 24.4 KB (24396 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:d5b261051d90f1c6fc10412d92b083cb58a2b1488dc10324ef3eba98d29feb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79987426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1940a3dfb079905f6ef17b109e1833701c1ca410fb84c1b9742cd5be168875`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:52:59 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Apr 2026 01:52:59 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 22 Apr 2026 01:52:59 GMT
ENV NJS_VERSION=0.9.6
# Wed, 22 Apr 2026 01:52:59 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:52:59 GMT
ENV ACME_VERSION=0.3.1
# Wed, 22 Apr 2026 01:52:59 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:52:59 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 01:52:59 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:53:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 01:53:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:53:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:53:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:53:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 01:53:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:53:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:53:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:53:02 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 22 Apr 2026 09:05:46 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c5941a502948ef06b21687352a13bd28db5a296bb0a7d25c3620f921a8663`  
		Last Modified: Wed, 22 Apr 2026 01:53:25 GMT  
		Size: 33.5 MB (33484313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb1dd966c5b40b59145cb6605a1300eaca855944cc6129194614e6d57f70d2d`  
		Last Modified: Wed, 22 Apr 2026 01:53:23 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dc18747806e003d805f5df7c4d0d9f2061824dc791e7631008e774a115a3d8`  
		Last Modified: Wed, 22 Apr 2026 01:53:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409def26cd531c77183e1c297de4d04e4d5c5e9e21d60309e36f06727f9b295d`  
		Last Modified: Wed, 22 Apr 2026 01:53:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb33fdc3f8c7d17ce7e1849c0a953df8f47a9362d635ef63fc877fcb50b8d57c`  
		Last Modified: Wed, 22 Apr 2026 01:53:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b2adda017aa8d779f3f5e5bc75378394e9980358a4894fa95abfbb239e62b7`  
		Last Modified: Wed, 22 Apr 2026 01:53:24 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa3dd83f5cecec1333262acc2f50ee34bc2445a791b93d8ccace8a11da9288`  
		Last Modified: Wed, 22 Apr 2026 09:06:11 GMT  
		Size: 12.9 MB (12900476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:1dd49d6f40690362bcd742b5b940b8dd2ffff625afd4018638abeb8c8c771b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08ea9c8ed9ee40086f88ad6daeeea50eca7f8f648b7c879a01c23cb1cf79a4f`

```dockerfile
```

-	Layers:
	-	`sha256:540f598d2a81bc934178fe85eba4fe7ad1e0fe8fd771b1c4418ff160811d4a50`  
		Last Modified: Wed, 22 Apr 2026 09:06:11 GMT  
		Size: 4.3 MB (4278951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445f71c020a1cb8e7a2fb66bbf4315a78bdf4e05d8a9fa92e8bf4f165db57555`  
		Last Modified: Wed, 22 Apr 2026 09:06:11 GMT  
		Size: 24.5 KB (24538 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; riscv64

```console
$ docker pull nginx@sha256:9a64c99fd244649293e9251275de3cd204c46e33e8a17db8f0a64cfe275b85ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69765732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c8fc42b8237c7cc31c9ba41a1bf86cbfa318cf8cf033ca00198ebdfadcd12d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 11:38:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Apr 2026 11:38:30 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 22 Apr 2026 11:38:30 GMT
ENV NJS_VERSION=0.9.6
# Wed, 22 Apr 2026 11:38:30 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 22 Apr 2026 11:38:30 GMT
ENV ACME_VERSION=0.3.1
# Wed, 22 Apr 2026 11:38:30 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 11:38:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 11:38:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 11:38:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 11:38:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 11:38:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 11:38:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 11:38:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 11:38:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 11:38:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 11:38:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 11:38:31 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 24 Apr 2026 22:45:33 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afa2e8452925c2d8680a8f3b6e42b99c586e66135743e876620bcc085e3cb20`  
		Last Modified: Wed, 22 Apr 2026 11:40:00 GMT  
		Size: 29.4 MB (29368328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b59beebb589da0cf9154ca92d2ace9702710e76095e5a9e028b327f90e19c41`  
		Last Modified: Wed, 22 Apr 2026 11:39:56 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2632c5ba4ed0a9f5f6d28ce6c7cc41e73586fc3d7851d71bf3983bfb37869d1`  
		Last Modified: Wed, 22 Apr 2026 11:39:56 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d6d3d4bdaa921861d8a9caa326c6246dc2314f1aa50f5c392a26b2ef3bf55`  
		Last Modified: Wed, 22 Apr 2026 11:39:56 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbd7499f409cfd237a51a868e81d9de3d4c6c2bc7c92c09d6156baf6490402f`  
		Last Modified: Wed, 22 Apr 2026 11:39:57 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4e8679479f5c95d3356de46b5f8b001bfe4190834b379077a7df6a9a18ce6`  
		Last Modified: Wed, 22 Apr 2026 11:39:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b502f400f209d80abe30f20c54f96a4bdd073e30b9ecc0930422cf9520ed5469`  
		Last Modified: Fri, 24 Apr 2026 22:47:10 GMT  
		Size: 12.1 MB (12112601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:39f058e6dd66c57bfe873332f518ed6193d774cc800d81ee51b6e740953e0001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4287688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fe7c6c77c20866084cb3234950c14a636d97029456c979d43d180f5bee20ba`

```dockerfile
```

-	Layers:
	-	`sha256:49740bf10d1a08a3baa326b75b573f42a81bce44c1d4e21179e165fd9068891b`  
		Last Modified: Fri, 24 Apr 2026 22:47:09 GMT  
		Size: 4.3 MB (4263151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad202ebabf52ca810e0098defa84dc0c33027891143122e0b1e25eb1dbdccbbc`  
		Last Modified: Fri, 24 Apr 2026 22:47:08 GMT  
		Size: 24.5 KB (24537 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-perl` - linux; s390x

```console
$ docker pull nginx@sha256:d5017d7b07d249be4ee009af366be424db84ad16afdbc9d5572568908ba34d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73685062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508fd32a424c1cd687b5de037dcc4f9dfc82f82b3d36add09e9987a533459c65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:26:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:26:49 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:26:49 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:26:49 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:26:49 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:26:50 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:26:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:26:50 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 08 May 2026 22:24:59 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b03df5ff49f009a8cabfddb18af44a2f4694cd15719407eec4c9c9bf539b6`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 30.7 MB (30653718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7780fd36b86f2fd663827127e327928c9816bf5738fd567408b97bae1951cf`  
		Last Modified: Fri, 08 May 2026 19:27:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21490a4124568a5aa7f84106ba4f0c89808702ff1607545461f3de38df2ebed3`  
		Last Modified: Fri, 08 May 2026 19:27:15 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d51ae9c5e3f0102859f06fed00738d708a295b93f1c7df39d8098e81e469af`  
		Last Modified: Fri, 08 May 2026 19:27:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3514432aae0926679a5f47a633a805c695af27cbb50bd07a16055576034b9e`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30b4517fdedc22ec08d4e7b57dc3bd665d01cd3ce777dd391a1b3ebe77d0d5c`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9240caaad666001f213968fa5e649df7f90e008ca7435e5774dd44e8fd76d9e2`  
		Last Modified: Fri, 08 May 2026 22:25:14 GMT  
		Size: 13.2 MB (13186389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:e639b516c0cd228639c7b6f8365f369a624859db09938be9c09c1a4d71527e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65105342364ba2ae8585657075fe4cc2548e97b5126ee357783df0baaa03308`

```dockerfile
```

-	Layers:
	-	`sha256:9a4d42d0dd2092ba3ea3a1129fb5f74ededc125326b1927006b89226bc08e319`  
		Last Modified: Fri, 08 May 2026 22:25:13 GMT  
		Size: 4.2 MB (4181557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a221f592bd6601be8c6b245ea058661e6298256ec84b3da67d49611f4b44601a`  
		Last Modified: Fri, 08 May 2026 22:25:13 GMT  
		Size: 24.5 KB (24458 bytes)  
		MIME: application/vnd.in-toto+json
