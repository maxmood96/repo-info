## `nginx:bookworm-perl`

```console
$ docker pull nginx@sha256:0343331288be595e45492a1381912135ed859d91aaf537807395c2a86c65be9c
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

### `nginx:bookworm-perl` - linux; amd64

```console
$ docker pull nginx@sha256:85460910745b131b6901d0ebc113e60affc12386bfc66f5abca5a483310a8bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83986615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506fe67058cfe3c42097667f1136b7e5d6d34fef3e370f12dd804de17699eab1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b00567da96412a0298328fad6b96aadd3bc9ca97e6683534da152b0b9e8a977`  
		Last Modified: Tue, 10 Jun 2025 23:28:55 GMT  
		Size: 44.2 MB (44151007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b81cfa547d78176e719c9cd387e35fbd95ce6e8500efb26d9fbcbac4dbc4f6`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc5dc8b475d9de62c94cf69a139df17aaf7fe7bac76b5133d8048a058fb3c3b`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979e6233a40af9a51ee2c9894bd42ebf78a79c87cbed70cc6a3840a0952f3d57`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a7ba8dbfee4f222961ad1449648ab46a6cea044e4cfb374450325ecee8f67f`  
		Last Modified: Tue, 10 Jun 2025 23:28:54 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e44235e1d55a34be577baa12271f067c0bf79ba4e1ca4e6ec484424540132a`  
		Last Modified: Tue, 10 Jun 2025 23:28:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb4a032cdb0697379c1a289bc00fd9c899204eaac5c9f02c7705c10f89a20c`  
		Last Modified: Tue, 10 Jun 2025 23:57:06 GMT  
		Size: 11.6 MB (11600880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:9ba31c9ae32e8cf441139fad49cb52d304994618caf86d80591200398ba12907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4442059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caade9d068b7524ee30770a7f30faba37ff799372c33e8cd59c2b8423d43192f`

```dockerfile
```

-	Layers:
	-	`sha256:07ca6c9669c267638c74f1d2c43d3271b95d30ebb24f947b542e43c3b325b6ff`  
		Last Modified: Wed, 11 Jun 2025 02:51:15 GMT  
		Size: 4.4 MB (4417760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57363f942145d205bf85aff24d0053fef83dd1199ce6220a81d4fe06c354b7e`  
		Last Modified: Wed, 11 Jun 2025 02:51:16 GMT  
		Size: 24.3 KB (24299 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:698b7642a888447082efba9ffdfb4cce72f44afd7c37fcf5c69728cefa37facc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73791230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43484526e341784a19e74dbc8e020558b36275f75d738024aa4fcf1a9d444c4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46797fbf58cc0b81cc9b7771818b680b0ef05e0b8db25c82707d0ae3404db115`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 36.7 MB (36684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aae346adc9677101f3edffe099a6b4fd82bb48e59859df64c17bd40094bc62`  
		Last Modified: Tue, 03 Jun 2025 13:33:55 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e419eac2af5a6a8710482dbd9964200576010f9bf13459d3cffb4cccae258b`  
		Last Modified: Tue, 03 Jun 2025 13:33:55 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81313324bc40c9ff1870b997938c05ae1e96c3820689e588dbff2c5ba7d9d3eb`  
		Last Modified: Tue, 03 Jun 2025 13:33:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c2160fdd519211a3b6b6e3af8ea54f7ecd36ef4bd02d573642372fe0923bb1`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1305aec6aa918862476aca8afa488cb94e962fd0f724edbb7351e803ac43e624`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e20cd4fddec31dcbd595c9539ccdefd3c939ef108424db64021bb6d0b68b0d3`  
		Last Modified: Tue, 03 Jun 2025 13:36:24 GMT  
		Size: 11.3 MB (11345611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:c9bb12e57f43319bb226788ff6e195277bfc8b8138bf225d41c3af9e73423b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd36bf37c5ac2fc04dc273931637fa7df34dca78aeec056ec8a7fd5ce80256e0`

```dockerfile
```

-	Layers:
	-	`sha256:215f4eb5519c8490b3422dd3925af586765a8ca55acd798ce442b1657e516fda`  
		Last Modified: Tue, 03 Jun 2025 13:36:30 GMT  
		Size: 4.3 MB (4320304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4f736386759b2985244788379d57379d25fe4d7f1f6639547e743ff014235a`  
		Last Modified: Tue, 03 Jun 2025 13:36:30 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:7b414f39610cd96450c53146e3668a7ef961d8773dfe2d1fc8e7a0262e600fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71982652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974c6de793fc06bd16a046c21a9adcdd34d3ebc14463388ecc2c4946dd9d478e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bb572a0a11af4f39dfd8eb45e71642ca3fcde29642ce9df06f863e7b83f8a9`  
		Last Modified: Tue, 03 Jun 2025 13:33:25 GMT  
		Size: 36.9 MB (36897031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e19bfcbb8eaf8c237ee7a902cdd903607e51567c45d29c04d75ae4176b47941`  
		Last Modified: Tue, 03 Jun 2025 13:33:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6c1d771821febd8991b1271fbc854aff03ea3a5f93e31d1ceb8ff7d07de18f`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741b3575b60399335c30492399eeee6237409930cdbbcaaa06238f5c993c6f4f`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9505b270af59be8a7ddf76baeb6a913e5f066f9718899c29ae87ab11d2685b5`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea089a8d9174c37fbcaeb61737896ad9adda31a39df9a2f26955f396b46dfc`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a269b4cfdee132a66f6e3e7a227ae7605bba4f8c03611b66f5e1e11890b0a`  
		Last Modified: Tue, 03 Jun 2025 13:36:39 GMT  
		Size: 11.1 MB (11148099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:c351eed688c5b03d91ff2466de63ea02f93900722b3a1c9135c91020b44b0493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b613b2832f95bd84b0e9a0da46103c283388563b05134216095d2b480998f6a2`

```dockerfile
```

-	Layers:
	-	`sha256:8d123aa0a256c8283aaa37372561e26cd823a238a4b0128385cebc712e6c65ad`  
		Last Modified: Tue, 03 Jun 2025 13:36:45 GMT  
		Size: 4.3 MB (4319729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50fc8fdf6d8bf60da69932173c6c1550f131ca54751430e566def44b89f8495e`  
		Last Modified: Tue, 03 Jun 2025 13:36:44 GMT  
		Size: 24.4 KB (24422 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:720bcf32f8ed68e87d866f92a1df8f29cdb2b739ac3b5433253fc6e428152410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80381094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d01f42f8baf3cdd43737f1190ec9d1d789bce72ec9ba4dd5c21114e963fa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a20772aff432be3d6f1d387ba4e04324ffc462018bbecac77da3b2777d6571`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 40.8 MB (40755222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c242ffc14bb4ca8740c858cc9c1a3efdb2fdd16170bf1ecbb04c28bba4a4df3`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e7af999d2a5102cb712353946abf19b5477ae9b1b7b243b01ed7e37e23ec3`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbad98902925c3029f8aab8dde441ff2fb39265909385453cb6fa545cba6b1e`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf85f4d417b9405944634427415aaec4c52a312997fe9ab099b69fd7f5c8756`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f78d9a3fb110d051d699e1a03dac4de9c223e528eb3e123d5f6b36af64dc0d`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b09a3d9de4716feb944cf5f3222887d4fe7f9e333ce22156580fdc10e4c0c8`  
		Last Modified: Tue, 03 Jun 2025 13:36:50 GMT  
		Size: 11.6 MB (11555994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:f629936703adbcf973c6e6a4a6a45f5ff671f7047a498c82430b0ef82de43715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b362470f7b08ac3cadbe0dfee85e9facc19aedbfc9da17608dd66ac0800091`

```dockerfile
```

-	Layers:
	-	`sha256:87524431e57ce46b1aea4287f5aa86dcfc730ec7045c6b41165fb00b68a84c22`  
		Last Modified: Tue, 03 Jun 2025 13:36:55 GMT  
		Size: 4.3 MB (4301571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a8da89dee2f300dc55d20567b56209ce3d5b18752f9143bae5285e1d7cdb34`  
		Last Modified: Tue, 03 Jun 2025 13:36:55 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; 386

```console
$ docker pull nginx@sha256:598e1ad8823fbd27ec21f67cd37908121d390fbce180b2889c3a8013cce495b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82367453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cb7f0f4c73edbd54835f54854bc897297a9bf616af59a06dc608937d9be5d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058a3aeb89e28180ddbe63deadf1eeb6d025dc8628edb3053932c82f4014ed50`  
		Last Modified: Tue, 10 Jun 2025 23:33:33 GMT  
		Size: 41.5 MB (41535325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff490355ee7c902ef816a5ff4875be7641c21b17cf3aba419bd18f61b59f1fec`  
		Last Modified: Tue, 10 Jun 2025 23:33:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2246ffefc86ba4746c6af208868df640736b771c06651879016b360bd985d7c`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c8349b2aa921aa0e3faf609d0a8caa0f0a72de3f55a487985583211635c00`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a1c84a0243c4450199b296217e43036e45dd187086a65f4e0ba169c984751`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24614574c9847062a87a8ac0c0bc34edabd7c594bfbc24c6d961f4bac340b439`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a5309d9f2105195cb2bdf8e39b72b6833d6b4767af61e0a1a6fbf7b6ff214e`  
		Last Modified: Tue, 10 Jun 2025 23:57:59 GMT  
		Size: 11.6 MB (11615089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:b8a83fbb63310cb9fb59140873892f600c47f6097093d4d23b09b50423272519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4465058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00317955aac6f22434d7a947a9e81db25e4ba05725d4127f7dd6d5eba72522e0`

```dockerfile
```

-	Layers:
	-	`sha256:7848f395d3a020c73c4551c526caeab39f1a1dbe640ca794e06e28cc88dcc756`  
		Last Modified: Wed, 11 Jun 2025 02:51:39 GMT  
		Size: 4.4 MB (4440821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6231f0aa5d38f996a1b734449b90b7c66990c3a450f4ab6997c5344444ee6c`  
		Last Modified: Wed, 11 Jun 2025 02:51:40 GMT  
		Size: 24.2 KB (24237 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:772867e1cb2001442a5dbf6fd4f505f2b254e959261ebe0ffaa6ae3b0fb7e333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79893707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c0e3938203ff1a7578d2270b28499999e3683edce5aca4b5b0fe5ee174648c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634e5a7d53cc239ea5d8a79d838bf180de94f86de378848dac6a79a21b86d29`  
		Last Modified: Tue, 03 Jun 2025 13:38:44 GMT  
		Size: 39.9 MB (39942299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf64beb8fde7ebeef4f4135d61ad864fbd827090525f8649df5c13f9dcac31`  
		Last Modified: Tue, 03 Jun 2025 13:39:05 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe59b42e453d5f896b8876b4c713cbe25be310c3e3c877e8522198b116d7a53f`  
		Last Modified: Tue, 03 Jun 2025 13:39:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d934921a4c2aa7d330220f8c282499586dcb9f068e15f3bd03861719c1f5ef`  
		Last Modified: Tue, 03 Jun 2025 13:39:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d431e1d57c76303da6c954f8c0fa8c604b85f9605a04dcc9941e541cff371019`  
		Last Modified: Tue, 03 Jun 2025 13:38:56 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68e5f8d7bb751132dd48667ef8d42a0b90f74ebb10d4a083e2eae5102699a1`  
		Last Modified: Tue, 03 Jun 2025 13:38:48 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c3b928f2b8fb0b567b61cce49b5f154f339c88b8128d120442f5c7d7b75e9`  
		Last Modified: Tue, 03 Jun 2025 13:37:12 GMT  
		Size: 11.4 MB (11434951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:5ebfa11287d81087cb13d151e1e8715f36c4ff2a6c44d418d8a086313ed08c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938fb66c67dfc237e74681b057596bae69030a751722e0519c98e21f0a99d42a`

```dockerfile
```

-	Layers:
	-	`sha256:ba9526cb24aaf198f454260815321e41e98f8b86b57ac13da6ea15a453ff1440`  
		Last Modified: Tue, 03 Jun 2025 13:37:17 GMT  
		Size: 24.2 KB (24204 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:4ed5b44fb8011bd6bd714119532980a2888200cbff61d3e9006c145ab216a18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89454709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d1f8876cffbd4534cff1595972c6738ecd39c6aa35c9253c1bf0509c2b9db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb68beaf28b31d4125e198b73721b53950424855a626db6e6d85eec23cb5f0b`  
		Last Modified: Tue, 03 Jun 2025 13:38:49 GMT  
		Size: 45.0 MB (45035141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a5e7b099e312a8f3a4e174b9a8631e92e2094421a767d5466d2342438d9cf`  
		Last Modified: Tue, 03 Jun 2025 13:39:06 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a99a1f7bdb1df72c4e38568d522f7bc37d9ef7e8c0738291ce6e5a306e1c0`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdc7c0bb01a76adbda1487943cddb03cf4b8c8dcccd607c26fc6c483fcacf56`  
		Last Modified: Tue, 03 Jun 2025 13:39:07 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deda79ae7b1d591c5fdb3154e1d8861de68b42a73a95cd2e48f95bc47ce86b9`  
		Last Modified: Tue, 03 Jun 2025 13:39:00 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4dc646707345602650be35647d39abe907eee0aa5d4e0d72e148953d070ce3`  
		Last Modified: Tue, 03 Jun 2025 13:38:56 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8700ab4ed434438ad38db90fd8c335b95efdd7cb737229ec52408e72dffe29`  
		Last Modified: Tue, 03 Jun 2025 13:37:23 GMT  
		Size: 12.3 MB (12348054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:4465be0a236f2d566dc853bcdf6e54c4987f76c4c28a763c45d7ef9ddc57b57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4356178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185cf08a08db74e1f4e3422ddbfe803b68bf4d23d87abf131b0ad24f39ee0d08`

```dockerfile
```

-	Layers:
	-	`sha256:f19c7d72c2e01e99cf9d738f6d42f4ea77a1ba4ca4af6489047bf6b0d2ef48f7`  
		Last Modified: Tue, 03 Jun 2025 13:37:28 GMT  
		Size: 4.3 MB (4331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3858750def68623fefec585d4db6c237dfba94f696a9d8c7d99f346a6759558`  
		Last Modified: Tue, 03 Jun 2025 13:37:28 GMT  
		Size: 24.4 KB (24379 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-perl` - linux; s390x

```console
$ docker pull nginx@sha256:b68131128468e53f75a07557c4489f16ae5c64dce66555350dbd5e8cef7fa10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79492997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ff73899fe1a9e5cbb5a6135895cb007ee6d47132e4b0d807270d3ff3df5736`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed072dc88396de1509d26d75d9a3c20ba7a6f49ca9436b089c63632d66d41a`  
		Last Modified: Tue, 03 Jun 2025 13:38:42 GMT  
		Size: 40.2 MB (40186261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ffd3d064e77be76ce39d4e75d6aea37b0a31caf2627dba9ea6bf2bdab8072`  
		Last Modified: Tue, 03 Jun 2025 13:39:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a921ab74b2f64db836339053a522203d75e9014deb64e004302dc7b203984999`  
		Last Modified: Tue, 03 Jun 2025 13:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a289311cac061d3a5f4470683bb31e7272eea2ef46030a320e2bdb48f8da40a`  
		Last Modified: Tue, 03 Jun 2025 13:39:08 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee806fb7164ec65b10a6d87be4a29404a009e5fd0ebe11ba0c14a4eb541e6ff5`  
		Last Modified: Tue, 03 Jun 2025 13:38:55 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac045fef514d40806090f69c0463ddd0510adc6de66e4d8d0424c847424f4f`  
		Last Modified: Tue, 03 Jun 2025 13:38:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1808ec90c6865015f4d5b3dbfddc7f1703a6e76872b1e8d0c641e2942fb707c7`  
		Last Modified: Tue, 03 Jun 2025 13:37:36 GMT  
		Size: 12.4 MB (12419327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:fb1ef0d29bcdd42626db7c11a605136367c2546483e6695d2de0c7cec5f45fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91864df62e6e42760a612710919f3fadc4dd5bec47ee44518297bf8bce79ec7`

```dockerfile
```

-	Layers:
	-	`sha256:298d4a76f810b297ac5d12345eb23787feacdce9fc91af7e92219f430be240c8`  
		Last Modified: Tue, 03 Jun 2025 13:37:42 GMT  
		Size: 4.3 MB (4311523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9abe5d0a8cdc0566ab686f1c9c5c7ce0a98834752a3eca6aa844171f493a49ef`  
		Last Modified: Tue, 03 Jun 2025 13:37:42 GMT  
		Size: 24.3 KB (24299 bytes)  
		MIME: application/vnd.in-toto+json
