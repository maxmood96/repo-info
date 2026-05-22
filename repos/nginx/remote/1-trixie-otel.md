## `nginx:1-trixie-otel`

```console
$ docker pull nginx@sha256:5fd63271b774f40168be355fcd4a2c2f34d4c6d9957f24046aac0003a79ca066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-trixie-otel` - linux; amd64

```console
$ docker pull nginx@sha256:d226758fdbc967524a9d86b01c83f1457f2e21aa8abce979945ca30f58f65233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66810195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca264e7434f79c3007862754b96d310b6d955eaed507c1840573d61ac9fd18eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 18:24:53 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:53 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:24:53 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:24:53 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:53 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:24:53 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:53 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:53 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:53 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:53 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:53 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:53 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:30:27 GMT
ENV OTEL_VERSION=0.1.2
# Fri, 22 May 2026 18:30:27 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830625e1ac85a8c72dd41b1403ea8210c7441aba69b752537d9a8a1b93ac87af`  
		Last Modified: Fri, 22 May 2026 18:25:04 GMT  
		Size: 33.3 MB (33314379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431d0092ffdcf1729150a2100fae1197ae414486b76bba246fe659a1b4a9b4e`  
		Last Modified: Fri, 22 May 2026 18:25:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a248c845e558f875ac57f77d4498bb33110085b63ec15e966d186a939c94a0`  
		Last Modified: Fri, 22 May 2026 18:25:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b1a2b17d83cb2af2014ba3d9841933a83f729eefe67c5d73dd6a47263bbec`  
		Last Modified: Fri, 22 May 2026 18:25:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45381ecb0e2f57bc356fba7bca792013750edff8d0bf00c07ac2c7f1f0786aee`  
		Last Modified: Fri, 22 May 2026 18:25:04 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd728be9eb1209aaccfb92774f28b57314202bfd8fde3c54179b84d60907d7`  
		Last Modified: Fri, 22 May 2026 18:25:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150b14e573931482a5f38451c2c9b9dc92d6ccfee0ccc3644712547d6fe74393`  
		Last Modified: Fri, 22 May 2026 18:30:35 GMT  
		Size: 3.7 MB (3711296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:1060a4e813115d8a93e0c6c6bbf6890cd1daa04f854cb2ae42f6796b7ef43632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc90a1e8e66f0da9785117fb98ae762e747c169454ddfac9b50615697db33cc`

```dockerfile
```

-	Layers:
	-	`sha256:a672425553d4af753303e36f5a166ecc5a2ede88e2ac8bcd666858e226e94bb7`  
		Last Modified: Fri, 22 May 2026 18:30:34 GMT  
		Size: 2.8 MB (2829062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd5f6a046d5dd5c9592f049cf32061ddc1d3f19c24ae467c8976f02d2286ae2`  
		Last Modified: Fri, 22 May 2026 18:30:34 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:81144817aed845aea74c576e4572f39c78593452af2022a4055572e127b0ab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64871049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0848e4f6cdccf6c919e86c2ed5563af3fad912b644d4c9697565a03b4c8a48a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 18:24:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:24 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:24:24 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:24:24 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:24 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:24:24 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:24 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:24:24 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:24 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:26:20 GMT
ENV OTEL_VERSION=0.1.2
# Fri, 22 May 2026 18:26:20 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-otel; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debbdc1e5f5c3980e8d0d8936161cc6ab868930161a7bef95aac7695b5942c86`  
		Last Modified: Fri, 22 May 2026 18:24:34 GMT  
		Size: 31.3 MB (31253697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39c8651bd4eb65b3fa3363dedb0108baa6555b23431b4df76c1f4b5084b2aed`  
		Last Modified: Fri, 22 May 2026 18:24:33 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9bb37e53dcf79e7ec3b7adcc3bfb7a270514ebfa1692925772e579d1f277d`  
		Last Modified: Fri, 22 May 2026 18:24:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58898093a3cda7d3f635e1e0eb75b8f25dceae461d85b8731e77282da8ac853`  
		Last Modified: Fri, 22 May 2026 18:24:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9891bc902ba0c195925bb5212fae899b0d001a9819552427103a757d8b6708bf`  
		Last Modified: Fri, 22 May 2026 18:24:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6067ff4dc560bd25bee8ac9fe0207b91e69a490d1b5694a1e3e909a02fcba05d`  
		Last Modified: Fri, 22 May 2026 18:24:35 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df1f254e994a4655710a603183b76d7befbda84a5d41509034f796ea448212e`  
		Last Modified: Fri, 22 May 2026 18:26:26 GMT  
		Size: 3.5 MB (3470834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:bc5270f42c5e046e3f7018e973657ad35bf631e21306ad7fbf24d0ab4a9af629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2854291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6427782d1cb5196b3bcc3a9e49d3b4b05e98e6756bca127b0e7bf695f0ec5597`

```dockerfile
```

-	Layers:
	-	`sha256:b703614d4ad8279a4f744a2ba847b57d847e7dec7567edd2b4d89659880f783f`  
		Last Modified: Fri, 22 May 2026 18:26:26 GMT  
		Size: 2.8 MB (2829539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0f716d8044eb819b2e9b33aecb0ee7a69fbf4244bca889186df402597f7140`  
		Last Modified: Fri, 22 May 2026 18:26:26 GMT  
		Size: 24.8 KB (24752 bytes)  
		MIME: application/vnd.in-toto+json
