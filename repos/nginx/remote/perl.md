## `nginx:perl`

```console
$ docker pull nginx@sha256:a32e23dcd4f159478e22612fff039a18cff4d612a13a4a7595dbec3c752aed83
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:perl` - linux; amd64

```console
$ docker pull nginx@sha256:38d83ffc4e6c3e5bc988332266b2fbc882ce81c028ca072d7e5f7302b112b675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83897188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c66f8150759a94aee453572e9e11bab40bc46e0e28565b5713f59f748c49098`
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:da0fca9f9b28869ac747cda4e84bbbae844b2c4cfb45d7d5deac86fca727e613`  
		Last Modified: Tue, 30 Sep 2025 03:10:34 GMT  
		Size: 11.6 MB (11599039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:aed7d6150508ed485f7a71600cd28d59a521cb42ddce29c86185c17fa2821ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f844f89ae8b209ddc678c195379ca8a87cce6a0a4bbc3b04fb33a4cb861d2c`

```dockerfile
```

-	Layers:
	-	`sha256:cb1cdf66fa025ed545e42d10a69517d692fc045d819d17b24a4bd554f3550411`  
		Last Modified: Tue, 30 Sep 2025 20:51:31 GMT  
		Size: 4.4 MB (4421265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef2a4c203f30c12ce3f4985e2cbb1b9282c7e2e38a12bcefa9deace10841e5e`  
		Last Modified: Tue, 30 Sep 2025 20:51:33 GMT  
		Size: 24.3 KB (24298 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:00b4da744a6404a7dc90a5a676e352b0c6b3648bb13ff01569606a656b50f5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73858138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573404a7c643165934640e7d3b2f7553f103302c274ae3a2f88d3cae02ef0c61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fc1b7f8729ba0e0a256ef23482cb8d34cd0e2729673a52b4269f17bbec6d61`  
		Last Modified: Tue, 30 Sep 2025 00:01:34 GMT  
		Size: 36.7 MB (36749265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff482a54f3bebfc206dbfffb43cdfdce2ac1895fe2fb4cd5fd3a1f2e79b939`  
		Last Modified: Tue, 30 Sep 2025 00:01:30 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179d6cb58e90ed7b366216d36181b89402a8062bbb1c6f4ff0d4db9623894145`  
		Last Modified: Tue, 30 Sep 2025 00:01:30 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e47b6fefe762bd14b9e032d19214a0ac134d8297011058d1187877fc3d5ad4`  
		Last Modified: Tue, 30 Sep 2025 00:01:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956f00f6de3bc1adf1ad445155e3f67ffcfae06ed9e8a9049a1f1dd278815f5`  
		Last Modified: Tue, 30 Sep 2025 00:01:30 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c530a9bf9ce3230bdf36cc5d9bbc56c612535f089e8dda21d362032fa0b5c`  
		Last Modified: Tue, 30 Sep 2025 00:01:30 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f0985bacf41bd5cef19570011be9754d3d8e598e25e7fb19b2cdc3af97fac9`  
		Last Modified: Tue, 30 Sep 2025 02:14:12 GMT  
		Size: 11.3 MB (11346837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:05a1327c01e432d65d79ece86a3125bb75c5c6fe20f9be389f0eb62cd8f9e376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4475649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1286b88154d8d9574f3fcd9f388304ad8344d8b75fe921d3f8cb17929181ca91`

```dockerfile
```

-	Layers:
	-	`sha256:7af8057464d79aca180ae2c610a29ab1c2b75e55f4a16777b1477196189fdcc8`  
		Last Modified: Tue, 30 Sep 2025 08:50:36 GMT  
		Size: 4.5 MB (4451223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21b0f802368088b61b680e41b66f5c039dfadcb2b2beb1a42f6c0cecb88b24a5`  
		Last Modified: Tue, 30 Sep 2025 08:50:37 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:533272ebf81dff8992b46c618dfac6c88d7ca475900d994d50784623ebdc8253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71922211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb654c2f447fe2fad0563216c8894513c1211422c6aa0749db8d4324497b1ba4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba69d0fe74d3311ba124fc7754e1329d004a505ae62df8d340b47417b6c0bfc`  
		Last Modified: Tue, 30 Sep 2025 00:03:10 GMT  
		Size: 36.8 MB (36839288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e37dfa48351567196c29230eb7bb10d0225d9ca64bdde161179e6cfb27acb`  
		Last Modified: Tue, 30 Sep 2025 00:03:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b609a15f0f113cb99e5f32bad6a0272e155aae912647822909c2972bc1ec3a`  
		Last Modified: Tue, 30 Sep 2025 00:03:07 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bca30f8e59343614d414eb3bcc33fdd23e04ebbbdb1e8e4b4155c4e18d6f68d`  
		Last Modified: Tue, 30 Sep 2025 00:03:07 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8687703d8f15aa32630e57439ee0aecd8e7975154bfa713b7776740f83dc7ec7`  
		Last Modified: Tue, 30 Sep 2025 00:03:07 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0118ea0658442230a583b9775e9ef3e6a4708c43efc24ed4add2dca0dc6c5c53`  
		Last Modified: Tue, 30 Sep 2025 00:03:07 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a3380cda7a598b915d028850fae471cd01619a51299263b3c72eb42bdc4e04`  
		Last Modified: Wed, 01 Oct 2025 08:37:58 GMT  
		Size: 11.1 MB (11144387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:4d1c5c3b33c552cb2f3b3d1106c3ae8867d5f80283aa7f515ebc440742f77feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4475074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82e205abb2ba8eae2dc505fe2cb7b56227661b7fef1f877c14b3f4a69ca4244`

```dockerfile
```

-	Layers:
	-	`sha256:f373a672cfe88b4460c29f37221ece73c783443f8728be0b0b753b83a1ac1619`  
		Last Modified: Wed, 01 Oct 2025 20:50:48 GMT  
		Size: 4.5 MB (4450648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d591a7d9b54d997bf536ba237ccef320808db0a8f58a94a7512bd6df0514aa74`  
		Last Modified: Wed, 01 Oct 2025 20:50:49 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:1d7068cd20ea7a49acf4b76b74f75631e31d80d717a5d086ba7276435ddf4968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80411290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d229011f9cd7b0e5efc90755156002865f5aef1a26c82ef70b23b6aaca427e8`
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:04cf3954c5005b247abdd52dc25f70d8a89898afcd3aa5de8d16b2374cc06548`  
		Last Modified: Tue, 30 Sep 2025 00:58:07 GMT  
		Size: 11.6 MB (11563219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:ec129c2bd8d56541e38c63a4d18ec2a4d056dc48ed9a96417c812dc054ca787e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4452232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60145d57e699c2573fdbb83a8eac18095a06ffbe249e9d5b9f608c17859058e6`

```dockerfile
```

-	Layers:
	-	`sha256:c99f62e266cc57955b1eb4833f36da19e95afcead0e98f28b8d49579c59afefe`  
		Last Modified: Wed, 01 Oct 2025 11:51:54 GMT  
		Size: 4.4 MB (4427758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591f5e36d195173468a97ad1e35aaf9df674eea0244df8a2b4cc8a77d752f71a`  
		Last Modified: Wed, 01 Oct 2025 11:51:54 GMT  
		Size: 24.5 KB (24474 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; 386

```console
$ docker pull nginx@sha256:37c3415434cf3f27bccded221ca5976e09cf7e2acb8089ee8dacd802ce032b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82294113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1668cbf9f8cc7a4020869550e54b1f7565d58c5e31e2eb701f159fd282dc3a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc50b1d50fc0102d8daa2e91aeb469642baf5222bff4c4a5da71ab75a7de3db7`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 41.5 MB (41458552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a70987e077b0dec376ce7c8ce04f5fdd6608ce9cf749cfcf651aed1413a3ce`  
		Last Modified: Tue, 30 Sep 2025 00:00:00 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fdd1d65ed1e4d95a20e94498807c286f161f494b62a3b8295d6df4c57e77ca`  
		Last Modified: Tue, 30 Sep 2025 00:00:00 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bb50711408de141cb3db4d24a200e303b8a59022b8cbef8d14da53fdb0069d`  
		Last Modified: Tue, 30 Sep 2025 00:00:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafc59fb0188cc96f8eb1182741e1af5dfb4c3e9f2f1992d623873ab89c64c4`  
		Last Modified: Tue, 30 Sep 2025 00:00:01 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e6d14b2e51324217226f892058791768f0d3aefce14d5b293f524e23b05045`  
		Last Modified: Tue, 30 Sep 2025 00:00:00 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b98e01bc88f326947df9c9e3b9360d262de9d0c9fd5806c7917aaf5b110d33a`  
		Last Modified: Tue, 30 Sep 2025 00:49:21 GMT  
		Size: 11.6 MB (11621330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:f5bbc11f35e672de77157a7d466e28f915fb8f1134c880793ba2e8cc8f60c048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e55f9659d1b9c44abb7f3e423cea85bf23f086ba6d45acc25ef10224564455`

```dockerfile
```

-	Layers:
	-	`sha256:8bc98636e6aaafe1d69a68ca47a806d3d05cfd395a140aa2d78f8fb8762c3884`  
		Last Modified: Tue, 30 Sep 2025 17:51:47 GMT  
		Size: 4.4 MB (4444326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d6f7fabf0ca1ab45feec5fa51e48497218ac03b05f5a821ef083f89d449a57`  
		Last Modified: Tue, 30 Sep 2025 17:51:48 GMT  
		Size: 24.2 KB (24236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; mips64le

```console
$ docker pull nginx@sha256:e6fd5a6b1f2f285fde59a77a3cd46e110fb67c5ca845a900bc297c3744751133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79815049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08cc723a00b699c57458d4b72962d311b337f6bde42ef887b78cad884e213d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7411c46a0dc61d7e6bae7bc70a9c49fa4e21d960db20e9ab38f02fcb108ced43`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 39.9 MB (39865467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c15b52732f3a48855eaf1410681394516dd7e45a7598fc82e4e10a4433a5b3`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e51daf6ab5b0b5a55c4eedc87956feccfcab8dad2acf1844f0e861ea9c03e9`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b7013b6c506b9b551b24c63a5d6610ca65b83842af0b97f2732c4841b3fc9b`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ba665a8c1834a348a444734a2c281307e6f5294b989b9a6f0dc3a271fc7892`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe01265668aa0f544634b05c35e731f956c23850c141d29b46e527f51f87e86`  
		Last Modified: Tue, 30 Sep 2025 00:15:30 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa16a661b7f57ed26bec8064dee16c5cac57c5ea93eb99858a0a493918e2194a`  
		Last Modified: Tue, 30 Sep 2025 20:10:31 GMT  
		Size: 11.4 MB (11431302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:af0164260323b64479d07193a08535a1f24255c1a9fa80698d3b39b2f4120174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327d7faabb7f59ac1eeb466d215a69a66b89875c8ca59e9f12952059d8caf2a9`

```dockerfile
```

-	Layers:
	-	`sha256:d7d49a3b04d179e278089c7c386de9d4645fbe034ca62b1f1dfaddadd8e64acb`  
		Last Modified: Wed, 01 Oct 2025 20:50:59 GMT  
		Size: 24.2 KB (24203 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:84c4c4573e5312f657f5c0886dad281f886e2d87defa7e96bec322f6b25bc71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89366871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39628b378cfd64341806281a9a79a18f81b2d358ae3dc76618890e88adef746`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07ff4d8905168f7be4f70b79b8d78b1f05192886b711da13e177e6ef2e9fd41`  
		Last Modified: Tue, 30 Sep 2025 00:06:50 GMT  
		Size: 44.9 MB (44944713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eab61ae26b57454ee0b087770579ef7c736c7d0521dfb0017d226e174262c3`  
		Last Modified: Tue, 30 Sep 2025 00:06:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a293c677b33bbdde2af7d501661390381ac768c35f544b32056ae53bea243`  
		Last Modified: Tue, 30 Sep 2025 00:06:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d1f0c37004737c8a21922112c8a861648a701829e1c9c26361b259a9bc6856`  
		Last Modified: Tue, 30 Sep 2025 00:06:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19a41dd04d97b90dcaab3112df11ca0d0372529198a9131c4ebd87eb6e8b0a`  
		Last Modified: Tue, 30 Sep 2025 00:06:46 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a50219ac1866fb7fa92a34d25810fb7a5a9cacfbd7d378247bed37973ef409`  
		Last Modified: Tue, 30 Sep 2025 00:06:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573d8668c2af4bfaa1ca43c756cd86530b38c2c3866040a602853fcce24abe8f`  
		Last Modified: Wed, 01 Oct 2025 09:35:58 GMT  
		Size: 12.3 MB (12348857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:0c799f3f5661a6e72476b1a13d8231a4ccd9a24e63f68b8b027c6dc157e94624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4487096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785b23ac1201a42a4d07582bb46b45e7fe09052db8d1f93e9ef07574e3ddc99f`

```dockerfile
```

-	Layers:
	-	`sha256:8225a934b00661e5409393cf87d87fa28f064062c8ab36c0eeaa265a96803e9f`  
		Last Modified: Wed, 01 Oct 2025 20:51:03 GMT  
		Size: 4.5 MB (4462718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532a59629b674350cbe4b016fe6f122e343a299062668fa01debb6ee6c89c7ef`  
		Last Modified: Wed, 01 Oct 2025 20:51:04 GMT  
		Size: 24.4 KB (24378 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; s390x

```console
$ docker pull nginx@sha256:2e98afc3e935428cdd31048dfb878dfcec2f9ea930a8cc21225d98aae8e05c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79436603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c6680a87eb1c991ebe0c0cf11e343ff4c110dff74ed8174e946f717a9b542`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:34:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6e64b54f7434d5fec374976e64ea099256c80de0c5adb18b6ce4f5af364662`  
		Last Modified: Mon, 29 Sep 2025 23:54:31 GMT  
		Size: 40.1 MB (40127287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c7ce84b0375ed8b4c90bd08b78a711fdc94e9b7a9ac71e0b2e67f594bd54fa`  
		Last Modified: Mon, 29 Sep 2025 23:54:28 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331ba5e8cc9a347fd7e05657666497498f77b2194d45a528601ab91fa255b4f7`  
		Last Modified: Mon, 29 Sep 2025 23:54:28 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068f2f77388899f63d43af3c58b96fac9be47bf5d7de3fefb389a61ca3257d5b`  
		Last Modified: Mon, 29 Sep 2025 23:54:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45737e96b6843af42d95f9ef716c5c94fe00f8bad5d457320e4b3bce84b06228`  
		Last Modified: Mon, 29 Sep 2025 23:54:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bfbfff8f1d1462060b5c230efb1d5996ebe69fd8d499613245aa27114c49a`  
		Last Modified: Mon, 29 Sep 2025 23:54:28 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b2652475b012fd58a7832260cfc7be2c2e0d9110b0c2d9759e9e3e10b628ba`  
		Last Modified: Tue, 30 Sep 2025 06:34:29 GMT  
		Size: 12.4 MB (12420392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:2bebd130270ba2950ca2b42339ab498e1e134785e13f1cd3a6c1a553e287ca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53d0eb2e5195729eba7563cb773a157e0acd84dbaf5daa45a4fec89460a0844`

```dockerfile
```

-	Layers:
	-	`sha256:3059137e73ed4e660e885185ae6b4044b2f3733a2892741d7ae1374b6e982d0d`  
		Last Modified: Wed, 01 Oct 2025 20:51:08 GMT  
		Size: 4.4 MB (4439550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd6e6524d788d479fa6e4a2730900b639a1fbb4e660289e170c537b0fd2bb50`  
		Last Modified: Wed, 01 Oct 2025 20:51:09 GMT  
		Size: 24.3 KB (24298 bytes)  
		MIME: application/vnd.in-toto+json
