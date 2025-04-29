## `nginx:mainline-bookworm-otel`

```console
$ docker pull nginx@sha256:4597aaafc78d8165801056222f5ef78a0cf4d2ab3b82b8763110aea6843de832
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:mainline-bookworm-otel` - linux; amd64

```console
$ docker pull nginx@sha256:384288a3bd456b0d72deb34ecb80a1af542c4f879cdceaa85dcef1a6e4776aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedad9e215c6ed7e7147d349301d24e9d3118a3f0cab0c8d890224487d1f0257`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Apr 2025 15:01:48 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 16 Apr 2025 15:01:48 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91311529275035c77ef310fe38a81841c8f3e0a324cf6a68d86b36f48a145d0a`  
		Last Modified: Mon, 28 Apr 2025 21:43:21 GMT  
		Size: 44.2 MB (44150678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e544d53ce49d405a41bd59e97d102d77cc5412a717b3bae2295d237ccdfb706`  
		Last Modified: Mon, 28 Apr 2025 21:43:19 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f21ed9ac0c04aa7c64ffd32df025f4545ab9f007d175ce82c920903590daec7`  
		Last Modified: Mon, 28 Apr 2025 21:43:19 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38f2ef2d6f270e6bc87cad48e49a5ec4ebdd2f5d1d4955c4df3780dabbf2393`  
		Last Modified: Mon, 28 Apr 2025 21:43:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6e9f4e4564bc7213f3983964e76c27e1dc94ceb473f04a8460f5e95e365d1`  
		Last Modified: Mon, 28 Apr 2025 21:43:20 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc5ec71e9d6d1a06a1740efb4a875b28b102166509c8563c90b48f7c5e0bcb`  
		Last Modified: Mon, 28 Apr 2025 21:43:20 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f6690554784ca7385586c729f900de1a2956492ddd15fef01e41b59455a74`  
		Last Modified: Mon, 28 Apr 2025 22:14:10 GMT  
		Size: 3.5 MB (3520409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:0f78e2c266df1b2183ec08607edb171e78496b3a367cb913e5d295710f642687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510e27b47eb7af84ac37774a87fd7b810368940e04feb7af0a7955e7dfea4219`

```dockerfile
```

-	Layers:
	-	`sha256:9cd2784ec9c244a84d871eb4631dfa459e694a33456db970bbb4cd97ee4fe264`  
		Last Modified: Mon, 28 Apr 2025 22:14:10 GMT  
		Size: 3.0 MB (2967055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5eec33fc460e63fa73bbf2adef78ef7fab52234253acf6b4c5b72364b6b7eba`  
		Last Modified: Mon, 28 Apr 2025 22:14:09 GMT  
		Size: 24.4 KB (24390 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:20fa983f8c0c91baa2834f1a999ab6c6d77b785ad3dd926f0ea2ecc19a426c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72182944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5326016a46599c38be0f481223c2a6b75ef788b69afaa2d9522c7a91669714d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 16 Apr 2025 15:01:48 GMT
ENV OTEL_VERSION=0.1.2
# Wed, 16 Apr 2025 15:01:48 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de29066b274e2ed2dac558eef4fd46026fc03a8ff10f161d9909224984e689a9`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 40.8 MB (40752310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf157fc31fe8cc4501ab2599d6e2364defae458486140e6c3612dc321882b07`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45096856395554482df00dc06f6ca412312afdce69f02c8d34b7482f309d5cf1`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c47aa231e326ee90e85d440f0007c902fd4b4c27d0d2f7a747dad7fe2939`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a9ced98467386fb8929b6d25a8ccd4d6e835370c456dc6e6d97155c98d1ca`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96c7b918bd5e8a6966d3e2b1d2ef2a284459902d33f7539fa3531cb13c7dcc7`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021efe32eb9897053ded1cd7bde2d0d50b0d2e2c6219c3b2b5d6d736dd1c8386`  
		Last Modified: Wed, 16 Apr 2025 17:07:53 GMT  
		Size: 3.4 MB (3359718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:c5534b8d65ea7a786213e6c4817f8b16183075b03a3363e39917bdcad14acda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7b75afb08b4ed24bfe35d4e0f703784dcf80e021f8be183b051ea200826ebf`

```dockerfile
```

-	Layers:
	-	`sha256:6ba7defce422626f8b395bd1c9b29f9b9362e19e7573acb46f2bb03167ff3d9c`  
		Last Modified: Wed, 16 Apr 2025 17:07:53 GMT  
		Size: 3.0 MB (2967507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01025a872846950ada867b9edf224aeb5d39fce7c5da78c8df2b05a9a0f49742`  
		Last Modified: Wed, 16 Apr 2025 17:07:53 GMT  
		Size: 24.6 KB (24566 bytes)  
		MIME: application/vnd.in-toto+json
