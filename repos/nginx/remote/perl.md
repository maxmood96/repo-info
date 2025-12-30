## `nginx:perl`

```console
$ docker pull nginx@sha256:fec8dc61e7ac54cc0b09bb7672cf2e65ca5abda112b31cb583a21c1547115d56
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

### `nginx:perl` - linux; amd64

```console
$ docker pull nginx@sha256:d600d12d66a55c94ee344dc6e858af7b740a5c197af0951f32d667a065b435ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71935901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d51e378bd4edbd5d43d1980c5fe18b8c72fe756e09e83c28dabf5edf877530`
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
# Tue, 30 Dec 2025 01:14:43 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:0bf8b182599105da09b8126be9d08cc75462227e4a434f741e5db98fd2e5db77`  
		Last Modified: Tue, 30 Dec 2025 01:14:59 GMT  
		Size: 12.2 MB (12159926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:706a27702804020f2f5a19f4a4e1fa1d5642defe6b2c2a21dbcb4a3920627c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4259423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2ac35efb16646cbbf739295e397249ae8b0729a4677c23d2e12dea4d1517c6`

```dockerfile
```

-	Layers:
	-	`sha256:692ea2bc3df08021e466b0561a18fb338f333e52c4b06db9923553e13633af63`  
		Last Modified: Tue, 30 Dec 2025 03:51:31 GMT  
		Size: 4.2 MB (4235201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f6c2bde63803794009fc36b25755469314f5dbe7279f4374a002f548605ba53`  
		Last Modified: Tue, 30 Dec 2025 03:51:32 GMT  
		Size: 24.2 KB (24222 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:73e4c5434400e330a6bc33bec286f26b320788501aa23aa585c774084d0ed0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63322515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0fc36270a8539604ba161d1fab19db0cf9065fceacb1a1462d378e352f0ac2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:23:46 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:23:46 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:23:46 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:46 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:23:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:47 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:47 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:47 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:23:47 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:23:47 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:23:47 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 01:46:50 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580a265caf20483eecc9a548428d438d769ee4fbe5bc87a2710afa0a6731cfac`  
		Last Modified: Mon, 29 Dec 2025 23:24:04 GMT  
		Size: 23.4 MB (23431589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89afcba65ee044e616624577147628d25db6c20aa3f7e565aec973121ed6df`  
		Last Modified: Mon, 29 Dec 2025 23:24:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768020a00d1da8662610527a1eb3624ac74d34dfc8952cb3414655ea588b9aba`  
		Last Modified: Mon, 29 Dec 2025 23:24:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ced1b250eb042d323f879276c2e5b15f590e58c7761b944cfba62301c5ae5`  
		Last Modified: Mon, 29 Dec 2025 23:24:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1198b44ccc7d1b3447ba896697e8dbbede8c5430add1a8f26ef0c434f34c4599`  
		Last Modified: Mon, 29 Dec 2025 23:24:02 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129827285b83a229f35df26ab915de862c69979416ea81e31b6f07e415f0fc4c`  
		Last Modified: Mon, 29 Dec 2025 23:24:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d1e9a0d8d7a4fa6b868ca12794eadaa05cf44289dcb3a8227999547b5c9615`  
		Last Modified: Tue, 30 Dec 2025 01:47:09 GMT  
		Size: 11.9 MB (11942184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:580baecbdd8b9a904c09746d3afc821bf8c5cfb0f122e7860fb7ad4660212490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f256cdc74193d62d3843cac471c57e79da25e2f9009791495b163fc899258ee5`

```dockerfile
```

-	Layers:
	-	`sha256:6d6f63e9333cf7b3335d86d083838b67e06f928ac5e43646cfe3fcb840b0585a`  
		Last Modified: Tue, 30 Dec 2025 03:51:36 GMT  
		Size: 4.3 MB (4267258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826ead19a580cc4bf1e3d5c2f5e6558fdc7314e493045eb4cdfcd7d67b6d22ff`  
		Last Modified: Tue, 30 Dec 2025 03:51:37 GMT  
		Size: 24.4 KB (24351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:e4dc7f5972d9cf163b3f8d763264bc214c4d3ecbecb69a6b8768d91f242b0ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61402907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc817731b3c5aa091279ff9786c35287c6d2a843c3e5cb9c9fbdb5907328faa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:23:11 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:23:11 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:23:11 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:11 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:11 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:11 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:23:11 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:23:11 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:23:11 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 02:03:47 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c7cef93217c27d4aa383c387a44b2dc4b30d45fc8f4fa85b77fd4f282242f`  
		Last Modified: Mon, 29 Dec 2025 23:23:29 GMT  
		Size: 23.4 MB (23435922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b692f2baada4edc0cf350abe0fa844434810e09ffdff91509d82a4a267f7bc26`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4561e5108fea834194f509144de6cec16caed07565b3e7622a29158d99114a50`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ca53a0192c4d81b3af91718add7ee619846302d34a0a2cffd35d33be1b6bbe`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e540886b10a6e2877110678911ca1067f82cb161529c23485c985022658f47`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9158a6025e45c4cd504747dc0e58c6550f8faa391865d78fd311dc49991e4`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71115e2ce06a7a9a1d941db13a433bc62b2053421068cc2fed379b4a521d8fd6`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 11.8 MB (11752387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:14ad75a4f123ec9963a8c932240d0b18c4b31241f884dcb3b4035a9a13258bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e400888a2986a953458500e654dc9e6062b455d31d4fa1c86e5dbcfe435f7afd`

```dockerfile
```

-	Layers:
	-	`sha256:41d4ba6612fad64853982d37b0bfd6c6dcc9d5636749d95a457ebc84c7ab2e36`  
		Last Modified: Tue, 30 Dec 2025 03:51:42 GMT  
		Size: 4.3 MB (4266779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d9c1ee3c10675d46ffce9cfb90794c5c664c04e03471545192424a0b82824b`  
		Last Modified: Tue, 30 Dec 2025 03:51:43 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:cc9c278c7483260c31ef2585a96a9e2d66e3f858a6611eaa1065429ea25c0264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70368240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4484d274e260ce6dde575acb6deeec39328fd71b64b42e0a7e2fcc6424217b0`
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
# Tue, 30 Dec 2025 01:16:16 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
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
	-	`sha256:feee741a0a0f62685bf76b99dd6034b8d4e937b616c617063bb4ba8696bc1a19`  
		Last Modified: Tue, 30 Dec 2025 01:16:32 GMT  
		Size: 12.1 MB (12104596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:7890e58f893abd2dc10aff9ac9aade1b7c7c134a15b7611019d0c5ed39e4a6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d1d8b1db6f4e921aec6c5aba0dfb08b6409e4e352410b8d3f4c3a3b11bf745`

```dockerfile
```

-	Layers:
	-	`sha256:81b48efa3230a33bfa4239d905051a393a0cf00350f752963e62ee455a71b48c`  
		Last Modified: Tue, 30 Dec 2025 03:51:47 GMT  
		Size: 4.2 MB (4241727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6dcc9c39ca6097982088b91f13c0c0d4fcf02e9182ef757e10d922f3e01621e`  
		Last Modified: Tue, 30 Dec 2025 03:51:48 GMT  
		Size: 24.4 KB (24399 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; 386

```console
$ docker pull nginx@sha256:ae6cb07d03684ad62c2810a62bcc380d08d7f6556af822e9c551062f7bfa9795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72196902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a725df320517a043af0d4e273793c5ef797f45d8bd5b2b0438f397e6b7423bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:38 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:21:38 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:21:38 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:21:38 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:38 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:38 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:38 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:21:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:21:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:21:38 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 00:22:13 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc973b4d2fcc8d560ee0723df45568a877abd5fe5e5336c1d0af08e1b1a5493c`  
		Last Modified: Mon, 29 Dec 2025 23:21:58 GMT  
		Size: 28.7 MB (28721179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2cf70fed1033c2cf1b92b969c16bd64ffe216e05075762ead96dd39001ace5`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d63311f8f3da00311ab5d3b73e19d7e36c7088e9aa9cb0dfd01673ccd8901f`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e5ba4d19e575fb112eee39d6d9277fdb53ceb76b8b00864cc4212556ba032`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ae44e7c6523efb6fa24f20ecb6f238163d8f786b4aaf4b839fb6cde69909`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dc7f5061137f43077de6d862949a5d16228bd2215b517105122579e8c5f98c`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666ab78ec1ff7c9ba49cb4eb5ba5786264aec8edd011a4baf1a4cd9ee8f81b7e`  
		Last Modified: Tue, 30 Dec 2025 00:22:29 GMT  
		Size: 12.2 MB (12178019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:a0e5721852e170b276655ece78c6f948692032f77d8c9e453da411650e2f1f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4286376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229f510b37c1ae998c33784243209c51e25da8fb1882466b64a8f95b90967208`

```dockerfile
```

-	Layers:
	-	`sha256:ee94406b8a4aeba12d01e0ecb4e8ff5b292266f8e739eaccc0686026980d8cde`  
		Last Modified: Tue, 30 Dec 2025 03:51:52 GMT  
		Size: 4.3 MB (4262215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68451316b023c5f0780a59fde7c70b19cbbc415e764937f9c18e64fcd3b2ab2a`  
		Last Modified: Tue, 30 Dec 2025 03:51:53 GMT  
		Size: 24.2 KB (24161 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:28336507e427ec876c4c8828086ed406c39e902480e077afd5930bb10a3f1ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76737590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d834267c3dcda95fd193772827d8bf6a7975e9b0f628b688a40c7cf839239614`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 22:57:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:57:51 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:57:51 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 22:57:51 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 09 Dec 2025 22:57:51 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 09 Dec 2025 22:57:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 09 Dec 2025 22:57:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:57:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:57:52 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:57:52 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:57:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:57:53 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:57:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:57:53 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:57:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:57:53 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 09 Dec 2025 23:12:37 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e2d3a8237a37afcc15655ed4fc7d321ca40e157b4a823c66fd8bcaf4420c63`  
		Last Modified: Tue, 09 Dec 2025 22:58:30 GMT  
		Size: 30.2 MB (30239602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35837f2879c6d3b2e58dbf14a2c447f377de9d2e771e42a4cdc033581a5bb4c`  
		Last Modified: Tue, 09 Dec 2025 22:58:23 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c4e4162e508518c8975fa3b328796702bac032bfb0a01259290c1dbae1b61`  
		Last Modified: Tue, 09 Dec 2025 22:58:23 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c45a0cddb50e2a7796b4b012d33b93de3a42d445cf8fbea7a250c80a1085ea3`  
		Last Modified: Tue, 09 Dec 2025 22:58:23 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373790764d18972bee235e7a43147c1d1f7bdd274b4605e92f6b6a46d5c53421`  
		Last Modified: Tue, 09 Dec 2025 22:58:23 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34cb78994405a7d6bdc77a5ff59cabecb8ede8cdc18c4e07134d1cf1b429f0e`  
		Last Modified: Tue, 09 Dec 2025 22:58:23 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6912da619619cc159d4d25e438fc27c12c7a4c247fda42bc964b9c828621b`  
		Last Modified: Tue, 09 Dec 2025 23:13:06 GMT  
		Size: 12.9 MB (12896497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:6efed55f9b9de0331bb27aeb212ed9ae7a42ead282d7e823b49182005f7cde6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dda4b8aa48aa975d6a5a33b98d39409cee73f7c7f470fc44c60fec2a3a3932`

```dockerfile
```

-	Layers:
	-	`sha256:2ff8103caaedd5f22f02fa3a6841e5cac39fd5996da0cf78a2299f572861b940`  
		Last Modified: Wed, 10 Dec 2025 00:53:20 GMT  
		Size: 4.3 MB (4273399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f02f39c7c4d55593203fe925c0130255f4be98202f44734e0f0ea0fcee2df5ae`  
		Last Modified: Wed, 10 Dec 2025 00:53:21 GMT  
		Size: 24.3 KB (24303 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; riscv64

```console
$ docker pull nginx@sha256:4ad3c164a52ca43db57e1a64b2097b4c47f8116e0d5ba02fe4cd9be2682c82d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66822480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8dcebdb78ba57c60a22ea19a2e0f0cdd4930b0ac66f37c9548032dc227fed2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 10 Dec 2025 19:18:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 10 Dec 2025 19:18:01 GMT
ENV NGINX_VERSION=1.29.4
# Wed, 10 Dec 2025 19:18:01 GMT
ENV NJS_VERSION=0.9.4
# Wed, 10 Dec 2025 19:18:01 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 10 Dec 2025 19:18:01 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 10 Dec 2025 19:18:01 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 10 Dec 2025 19:18:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:18:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Dec 2025 19:18:02 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:18:02 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:18:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:18:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:18:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Dec 2025 19:18:02 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Dec 2025 19:18:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Dec 2025 19:18:02 GMT
CMD ["nginx" "-g" "daemon off;"]
# Sat, 13 Dec 2025 20:19:19 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64a00606304d9b273eb96bd70caa50961635b77abb572b70456f5a6d4f7efb6`  
		Last Modified: Wed, 10 Dec 2025 19:19:42 GMT  
		Size: 26.4 MB (26436010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22bbb0cae51bcf9da51c64f507176d08f5e80711cf5ddb689dc604cf621436b`  
		Last Modified: Wed, 10 Dec 2025 19:19:40 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad22a0c0dbd27b77a9d5883da027c810a509ae17453000bf944cc84860f1f512`  
		Last Modified: Wed, 10 Dec 2025 19:19:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8c4875db57df8b99faace1523d240ee756040459e565bededc73f5585166fc`  
		Last Modified: Wed, 10 Dec 2025 19:19:40 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05800a35a17a24b857cea4ebab2d3b851f0d3ea15b51ba5b8e55888683012440`  
		Last Modified: Wed, 10 Dec 2025 19:19:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f30c98027cb41c7812b4f8cc670fd150d6203d611fa610e794c8e5ca27ef4a`  
		Last Modified: Wed, 10 Dec 2025 19:19:41 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bce3e093662ec9de46376c8455b903ddf5ce6cde885b878e29b9d59b899005a`  
		Last Modified: Sat, 13 Dec 2025 20:21:02 GMT  
		Size: 12.1 MB (12108705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:80b5aee767fad7dcbafdd36b4ddceaf56b9366f0f9482b75371e8477a24f4133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8dd230855a0e2ea20869418625ffac4f91bbf970ec2de950e35c20ad776a6d`

```dockerfile
```

-	Layers:
	-	`sha256:5cc576ef3c4e9f2a9e433b12282dd0e96d41a699efc463539aad3a2f69c80f9f`  
		Last Modified: Sat, 13 Dec 2025 21:50:51 GMT  
		Size: 4.3 MB (4257635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aec860e96d350fe341cc1a06ed794e46829cd1767cf96ae21196603833c912e`  
		Last Modified: Sat, 13 Dec 2025 21:50:52 GMT  
		Size: 24.3 KB (24302 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:perl` - linux; s390x

```console
$ docker pull nginx@sha256:5082f44f88bb4bb47c1d75de3b94da98d2426d46fee4510fe2faae3c85352082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81b86b75ab9e6bdb44d13fb2f739b48f0b48a1031169efddcff9d773fb997ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:21:09 GMT
ENV NGINX_VERSION=1.29.4
# Mon, 29 Dec 2025 23:21:09 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:21:09 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:09 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:09 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:09 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:21:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:21:09 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:21:09 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 30 Dec 2025 02:12:22 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687349e68fd274f216a399a195ef5716c48b0d0ec70f4484c87a7f7c2d88b6e7`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 27.2 MB (27151388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9cae26287dfd2a4bce01d5a1d23fcbfcdfd2fc648348d9a07065684e46ce22`  
		Last Modified: Mon, 29 Dec 2025 23:21:28 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c2f9ef58c73ca013a126a2d4b5d27d2a6616e906dbfe990544010ce31f5203`  
		Last Modified: Mon, 29 Dec 2025 23:21:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2785d8f07f013693130614978974f942e9bb291be4d44bd3bb142a5c98ae6cf3`  
		Last Modified: Mon, 29 Dec 2025 23:21:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa8c90d0c69422aab71e2e9bd4c0451816ca3f7026000fd19bb9b0bf7f1c7e3`  
		Last Modified: Mon, 29 Dec 2025 23:21:28 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8931918967d5394b8c9b3191702b1a895cc48ac5e6ce6b7c7f49f8b33a9eda86`  
		Last Modified: Mon, 29 Dec 2025 23:21:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1553cc672c44ea3829243bc67909731d485a2b42aa216f10d861ce8dd78e4`  
		Last Modified: Tue, 30 Dec 2025 02:12:44 GMT  
		Size: 13.2 MB (13182450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:perl` - unknown; unknown

```console
$ docker pull nginx@sha256:d19da8e1ac34d553e1144060664652b33668cccab2f995294a729cb9292524a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606eed60b95120d6d4814c9cb1da2a937b265f5ba1945cb5dec881d3fc60ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:724a2f64e0730fb424e67907e1711126370a1967a462c73b78816be04fb278b9`  
		Last Modified: Tue, 30 Dec 2025 03:52:04 GMT  
		Size: 4.2 MB (4176041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4c6797a9e3ae67d0591d5e2e8b5c61bed4891e90d41c2111d85b1b103d39dd`  
		Last Modified: Tue, 30 Dec 2025 03:52:04 GMT  
		Size: 24.2 KB (24223 bytes)  
		MIME: application/vnd.in-toto+json
