## `nginx:trixie-otel`

```console
$ docker pull nginx@sha256:77d114fce844987cb47752e6b4bc7a3111fdd9763277749d2bb2b61147a08d3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:trixie-otel` - linux; amd64

```console
$ docker pull nginx@sha256:2060d688bdefcf0253fa6ce932b66b2a5faae29afa599de3cc471187af854388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66822238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5dab016499120a51d6c4af2e5ea805e56b02350839ed119fc950e9997e7808`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:44:41 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:44:41 GMT
ENV NGINX_VERSION=1.31.2
# Wed, 17 Jun 2026 22:44:41 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:44:41 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:41 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:44:41 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:41 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:41 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4bba39eed68bcc887d119ec5079e9824c0a0e4602e6443bee1df396eb9181437eae481e83d533475951e39675d6e1ff54901bdd208262c4b34e74f5c7984e82c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:44:41 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:44:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:44:41 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 17 Jun 2026 23:12:02 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 17 Jun 2026 23:12:02 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4bba39eed68bcc887d119ec5079e9824c0a0e4602e6443bee1df396eb9181437eae481e83d533475951e39675d6e1ff54901bdd208262c4b34e74f5c7984e82c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da80f8205ea29005f2d75a4856d9df92a4ac4767345d94195a66b424dd3546d`  
		Last Modified: Wed, 17 Jun 2026 22:44:51 GMT  
		Size: 33.3 MB (33320957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5e3151b8c01ba13062f63720c4beaf37aafb6ba260e5d6fcd4ecafba5a66d8`  
		Last Modified: Wed, 17 Jun 2026 22:44:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3461bb3286189e9b1280465c4ac2594ba0cf782626e510b7279fd2b46fb88d75`  
		Last Modified: Wed, 17 Jun 2026 22:44:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99181f19640fe66e1bdb5fcc2d2b9ae60910350eba8a55ccd1c00d4c3fe01ffc`  
		Last Modified: Wed, 17 Jun 2026 22:44:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d78dceaedbae0f3297cfec4de550203fe2e711d1fd6bf08d55e5aec5c0960`  
		Last Modified: Wed, 17 Jun 2026 22:44:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82e83b01f69cc20dce86e9d334fd0ecf09ce30233bdbc1698d82bde65e986fc`  
		Last Modified: Wed, 17 Jun 2026 22:44:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1a95a9a82984dad8723dd4b3293d832b505125673e5f4f56b18a42e511dc8d`  
		Last Modified: Wed, 17 Jun 2026 23:12:10 GMT  
		Size: 3.7 MB (3711268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:3b0a88035c5a98f9b9829213401d5e6154a63ccb293c296a3f25998a3b53264b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4f4247a75225c1fd53a8f327106708e8a285a60b0571c8b543714a297cb9b`

```dockerfile
```

-	Layers:
	-	`sha256:af09adc4dcdc2c6145ce2ced73e112951fa1b1f2ad58d36fd89e33ea4f178edf`  
		Last Modified: Wed, 17 Jun 2026 23:12:10 GMT  
		Size: 2.8 MB (2829170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dffd50531e4247bba989da6dfb920d2b3daac88e108678a4113c9e5b08abf0b`  
		Last Modified: Wed, 17 Jun 2026 23:12:09 GMT  
		Size: 24.6 KB (24555 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7f3197052790a26329f109d9a2279a22bb765eaf36e8f3da9dde908f076a03ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64885536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc664d31edc94b1c5879afa3ae8690b2fdad3387829dce5173d3ba821cc090f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:32:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:32:37 GMT
ENV NGINX_VERSION=1.31.2
# Wed, 17 Jun 2026 22:32:37 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:32:37 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:37 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:32:37 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:37 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:37 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4bba39eed68bcc887d119ec5079e9824c0a0e4602e6443bee1df396eb9181437eae481e83d533475951e39675d6e1ff54901bdd208262c4b34e74f5c7984e82c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:32:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:32:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:32:37 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 17 Jun 2026 23:12:34 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 17 Jun 2026 23:12:34 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4bba39eed68bcc887d119ec5079e9824c0a0e4602e6443bee1df396eb9181437eae481e83d533475951e39675d6e1ff54901bdd208262c4b34e74f5c7984e82c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a97a34923579ff611c64a0238f23f3188035cf7cec2e0569512a1df98ece67`  
		Last Modified: Wed, 17 Jun 2026 22:32:46 GMT  
		Size: 31.3 MB (31261560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef4315fa7b7b50bd3bd6163904d40f5836a815dcf4724b7c43343341787b6b0`  
		Last Modified: Wed, 17 Jun 2026 22:32:45 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43899da0956326363f83fcb7030b8beb24c9cb4988956f7e3460af72897bc23d`  
		Last Modified: Wed, 17 Jun 2026 22:32:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572aad3b769d6fb7761645a84a7e2ed40e4f9846f3704984e365a06051e666d8`  
		Last Modified: Wed, 17 Jun 2026 22:32:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae94b355a6370b4678ced3abda1552aab42553412bd0be15555990490a1eafd`  
		Last Modified: Wed, 17 Jun 2026 22:32:47 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e1a52d6c50081832507cf880cafe9cafb830d8c92c07a593f78024dee8a117`  
		Last Modified: Wed, 17 Jun 2026 22:32:47 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5515e9385f5babc4a90a081c1f7f9483a9727bef44e1b856f03b1b510febe4`  
		Last Modified: Wed, 17 Jun 2026 23:12:42 GMT  
		Size: 3.5 MB (3470848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:6b4bcd35b950f75cbe35e95b3fa965da1587b6bf38afa1652a99c233853fd762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb452ca711cfcfbc9cc3c532f77ffe7447566354a8a01c1dc760a87225eaf67`

```dockerfile
```

-	Layers:
	-	`sha256:b34f419ad2f7573eab47705ea20f756866ad53efcca9bd5c475bd40d1221d065`  
		Last Modified: Wed, 17 Jun 2026 23:12:42 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d18d0b75e078999635a55cb5b4ae97326ae73a9fd9cf2ccebedb2a5fbf6bf67`  
		Last Modified: Wed, 17 Jun 2026 23:12:41 GMT  
		Size: 24.7 KB (24731 bytes)  
		MIME: application/vnd.in-toto+json
