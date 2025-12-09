## `nginx:trixie`

```console
$ docker pull nginx@sha256:39474e84c4626cafe5b060db347154b46e588fc1f79176af7e20a7e1d76f0436
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

### `nginx:trixie` - linux; amd64

```console
$ docker pull nginx@sha256:2408d7585ce328442960405617452c9db1016caa76659b2ab847a8c4374d14c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59751647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177015cbaee5383734c41f511a459f016566bee4f295e07881f68a569613ee9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:39:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:39:15 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:39:15 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:39:15 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:39:15 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:39:15 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:39:15 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:39:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:39:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:39:16 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:39:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a9db0de3080e3d0cd10ae59ebcd4da0f719e77fd263f3c10ee92202cbf89c`  
		Last Modified: Mon, 08 Dec 2025 22:39:33 GMT  
		Size: 30.0 MB (29970552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0da823c3c67d772bb4a4d32cf0297d7feb2e289ef7f3e02eb5564d7a636bc9`  
		Last Modified: Mon, 08 Dec 2025 22:39:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1907fe38b1cfe3c372f2fa47d2548cf3e564eeb7d64b7c3242066fb0eff8df13`  
		Last Modified: Mon, 08 Dec 2025 22:39:31 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25e9944b727f979f254e2f7fd6454605c84f54228a9eed4c27a78603df8fe34`  
		Last Modified: Mon, 08 Dec 2025 22:39:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5bb6a6b3643b76bd6b6031333d5654a860c33cec64751bf8c6c0ef6668248b`  
		Last Modified: Mon, 08 Dec 2025 22:39:31 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc422329a3e06da149a865b7784abd1d36b8d9353755c9ab516e0f9182add0b`  
		Last Modified: Mon, 08 Dec 2025 22:39:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:b0a2f80e246319fb3ee2dab9490085adf3427df0837b3623f0aa78c904163770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fced8811bb4d56cd4ae2d2a1bc5e27be379ba9fe35d002f8ed864b5c2433d0`

```dockerfile
```

-	Layers:
	-	`sha256:62fc35a6c726952f541f164412a4134a08afd6a5d66fae2b3dac8b286f399f45`  
		Last Modified: Tue, 09 Dec 2025 00:51:13 GMT  
		Size: 2.8 MB (2811745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ffa54e000977dbb2a3b87541899039d6cb5e78f62f68db94ed6ed88ab2e5ccf`  
		Last Modified: Tue, 09 Dec 2025 00:51:13 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:09828e86be42e7a4a99bf8a369a2a1ab86495bc32dd4518410a5af95df235cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51360876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b5a0ac149d2f6cf2bcfd14877828d383dabc9338f7cda963cb31b67b8eb84d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:40:18 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:40:18 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:40:18 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:40:18 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:40:18 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:40:18 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:40:18 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:40:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:40:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:40:18 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:40:18 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69d135cd536a4669ba178035dcb59aea1f125dec729bdfd5d8a7d5c4f29162b`  
		Last Modified: Mon, 08 Dec 2025 22:40:43 GMT  
		Size: 23.4 MB (23412091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3362b2d5cd3203638ebb0deb224edf01a25b1c5b20812e2027e8c24091b77921`  
		Last Modified: Mon, 08 Dec 2025 22:40:38 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b7bd5ce506a14196158e59a44dab790dc5a778ee80048f60a9242721a7075`  
		Last Modified: Mon, 08 Dec 2025 22:40:38 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d817dc6e733db415f4a77605f303b073a3e4af98020cf559bdb9196831d90c`  
		Last Modified: Mon, 08 Dec 2025 22:40:38 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90ebdc11074767bc6fa3f1652ae7d14da56500db0e23998539b0e294c51e7f6`  
		Last Modified: Mon, 08 Dec 2025 22:40:38 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0addb67ef565db6e47945271cdda804067542c79ad519c2aff5b1b478a270d12`  
		Last Modified: Mon, 08 Dec 2025 22:40:38 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:b87f8cce40ae8c8149814339e0de82c692f3e692f13715fb4e5dbb6f6c649e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8903b68236b8fdeee86550b90d04e0152ae7edf867efd67dcb725d840ec49eea`

```dockerfile
```

-	Layers:
	-	`sha256:7cbfddb4b0d45a022693763bd80a978d833692148080e1dbb4aeb75a94e13e20`  
		Last Modified: Tue, 09 Dec 2025 00:51:18 GMT  
		Size: 2.8 MB (2837885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70306221b754d1e0fae843a9cdc75c36ae8e2d27d3977aaca8f598dd3f549043`  
		Last Modified: Tue, 09 Dec 2025 00:51:18 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:2493792e31666aa0c5cacaef2b86f1792b99d41f92ef902f059c7c2bfcea65cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49628246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ef0b46799032a63c3fcf3524d7a0bdeff7dc9c7a4ec17fd7fb5d997581d4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:43:53 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:43:53 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:43:53 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:43:53 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:43:53 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:43:53 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:43:53 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:43:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:43:53 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:43:53 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:43:53 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff219d870a98f7074afb48bd4f24afb2c28256ef6efe2c73ef2e6a37a7aa5b8c`  
		Last Modified: Mon, 08 Dec 2025 22:44:08 GMT  
		Size: 23.4 MB (23413637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c0a60d20627c986b3254b97180984accb91ec1813225c763fda8473dc6405a`  
		Last Modified: Mon, 08 Dec 2025 22:44:07 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b0423e055295ac01d044edc0c8c92ef202cd34111b48ece7c5632d0bd5077`  
		Last Modified: Mon, 08 Dec 2025 22:44:07 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a2779c823c3d85129452941f9104886a50c31bba34ee3b83d7b8277b6dcf8`  
		Last Modified: Mon, 08 Dec 2025 22:44:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed0bddbf493b70a410c45ce838367730797613afc22c4ee5b7c3c957e7da069`  
		Last Modified: Mon, 08 Dec 2025 22:44:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e47938ea0fc062eb9cfdb6265f1a1edfb4bb89a4aecfa4d50e1423cd7eea59`  
		Last Modified: Mon, 08 Dec 2025 22:44:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:ee65cd708c66918dd6404deb16c739bcce12a29c49339fa2aec79bfd28c42f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efead2836da5734f3b26d9236527067fecfaef8f96d7a41f95e62fdcaa920e2b`

```dockerfile
```

-	Layers:
	-	`sha256:dc6561e129b083373f5ab7e232a5b3959a90476617f28015352b23d246f39852`  
		Last Modified: Tue, 09 Dec 2025 00:51:23 GMT  
		Size: 2.8 MB (2836630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daa484df40f2c75b33b28b36dd4f4143cf8989f02c65e566b1c3a8e71aa9e88`  
		Last Modified: Tue, 09 Dec 2025 00:51:23 GMT  
		Size: 34.7 KB (34672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:d95ee6262d5a7bdec2c351c02bce1f36adbd381a406cddbdcc9c932f012ce2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58242324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8ff4f5fd469aa634bc26494719388bae785e72270ca155a6db025167cebac1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:38:48 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:38:48 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:38:48 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:38:48 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:38:48 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:38:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:38:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:38:48 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:38:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27c2fd6129752216f8fd7ef98ff6e14cbc0f9e79a71f0dbf65309886164b600`  
		Last Modified: Mon, 08 Dec 2025 22:39:06 GMT  
		Size: 28.1 MB (28099103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53652562f6a510c2511a13f6bd2a67f4864d73369d0ff50554b580e48134367a`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50375d47b78d35a8a654cfea2911c19532fadf601166f311d0cafce908f5e80`  
		Last Modified: Mon, 08 Dec 2025 22:39:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a8a370883004274a7617d82b492ecf8be4bac8786bb42440288853bda8b335`  
		Last Modified: Mon, 08 Dec 2025 22:39:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ad1ba33ced98fab1693aa6f06374f34a5672eaf2f7cd32964a57e29e55d0de`  
		Last Modified: Mon, 08 Dec 2025 22:39:03 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c1cf7ca883f8ba11dc5ca03fdd42cd77700d56e5c577ff7b50eb2252947a`  
		Last Modified: Mon, 08 Dec 2025 22:39:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:99dba31b5bb9379bbc04819d5c0a6083406c3bce6bb897aa5adb4201a12de8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c229a66864ef85a3545651fb5f229c27f0398b2af8902b14ab4bef96ea6d335`

```dockerfile
```

-	Layers:
	-	`sha256:08b64884c3ee0cb86b3d727f3273507356319a7a49e6a989dd8ff692e1adc0b7`  
		Last Modified: Tue, 09 Dec 2025 00:51:28 GMT  
		Size: 2.8 MB (2812229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cf21926a214a1733663906983bf492ac6d712751e11b05e26d40a569f0e1f7`  
		Last Modified: Tue, 09 Dec 2025 00:51:28 GMT  
		Size: 34.7 KB (34720 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; 386

```console
$ docker pull nginx@sha256:32911655ea392c6291420ae920e398285c43cec129166e421a518c497be0a942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59989761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a095373bf77030417ea7c0c9ea294fda57a4284fc86558f0ed6bcfb8636c39`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:37:35 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:37:35 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:37:35 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:35 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:35 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:35 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:37:35 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:37:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727ed835843b29c21e08c493a05c799abd00cf248015b4efa2b93f161fff5ce6`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 28.7 MB (28692097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b969f3342e492c2a7305efd0bceac8c6b510afa4b26a1a8157d752e414cec73`  
		Last Modified: Mon, 08 Dec 2025 22:37:50 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3700ef1419a03db4df683966008d7eb94760b26d4e5e9533be4953fac403d12`  
		Last Modified: Mon, 08 Dec 2025 22:37:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1b9663dfdb6b7d04c60adde939ed3eb42732681eba97f99450318d0b6f39d1`  
		Last Modified: Mon, 08 Dec 2025 22:37:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa4989a0d080049d8f0099d7793a1c4cc4a82731ea306f2577368fcca9d2bbb`  
		Last Modified: Mon, 08 Dec 2025 22:37:50 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e63ccaba439f96ce82e6ad87831656eaec7b0d27b4fdce94b792522dd0bad3`  
		Last Modified: Mon, 08 Dec 2025 22:37:50 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:bdc36aca8c72d1431671c54372894bb39e6e2815fdf7ac5cf802ee4c02bd040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3009e013d8ae01143237e193e12266dc09923eb2cc3c18cbf62b6738a34d4f8`

```dockerfile
```

-	Layers:
	-	`sha256:b6d0e3dc6d6da363232036cd7d12f19fe196d723f78b22262873a144b602bcee`  
		Last Modified: Tue, 09 Dec 2025 00:51:32 GMT  
		Size: 2.8 MB (2831581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cccbc22ed474baaa20178c8a8b09aba5576a499880eb9b8daf22296c594670df`  
		Last Modified: Tue, 09 Dec 2025 00:51:33 GMT  
		Size: 34.5 KB (34482 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:a4f9edd24727204b0313b7e6df93bea94b161d29310831df463a2294560064c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63817066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e5cf473ba099b0681c1d1b0f0fdc75f0183d9ee839e15025c3b187f0624811`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:18:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 15:18:11 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 15:18:11 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 15:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 15:18:13 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 15:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 15:18:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d912651b28a1f4550f9027605087cc0b23629661ff2b51880373e625d7ea8`  
		Last Modified: Tue, 18 Nov 2025 15:19:03 GMT  
		Size: 30.2 MB (30215610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbba70b7652397310f840e280558d4e3dc1cca4fb7f3f2d55ad0d3315177121`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee77fdcf2dfb637465abf0fd1d0919e741c1c17d5aeb4336cac727a01de857d8`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84bf1fb0e81c24876666f7f8042ae7125ae059e487e5c6dcdb6f57e1570540`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c66213f80855923053c67ce2928b6d6944f278d50f258905642b0d31787455`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c1cb8f543bbb52d94639a15b6de03b238f7ce458d6f0d1695847ef82919a5`  
		Last Modified: Tue, 18 Nov 2025 15:18:59 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:3c8658e7455c4b5fa268c6b7fc3073804b008a774245ea938708675b0ab99e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2e56352c08f5773c055578c4249e8ecabdc6fc2762e4344eabf0afdf57bd9`

```dockerfile
```

-	Layers:
	-	`sha256:541d987323ac4a6d147155db29e06037053dc559b50749e65d4931646c3b8e78`  
		Last Modified: Tue, 18 Nov 2025 18:50:52 GMT  
		Size: 2.8 MB (2839275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542e041c49117c8c502451c174507632129f1ae75d642f593c1b5e6248ebe8fe`  
		Last Modified: Tue, 18 Nov 2025 18:50:53 GMT  
		Size: 34.6 KB (34624 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:2eca83f563c1b416ec37c092ec3f3903cf17aae8ce65305f1ad219a4e3024231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54686055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3046763668511eee4f4a7b1d9fb676e2c488842245e57076cd64c48dd3d522`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 12:58:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NJS_VERSION=0.9.4
# Tue, 18 Nov 2025 12:58:08 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 18 Nov 2025 12:58:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 18 Nov 2025 12:58:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 12:58:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 12:58:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 12:58:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104bd6b25ed0570faf0ecc12fd9704f33039bbcfdbc9bc1d32371e739d12ceed`  
		Last Modified: Tue, 18 Nov 2025 12:59:51 GMT  
		Size: 26.4 MB (26408325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa69b7788b2fb7e0c32101b1d39f3fb69d9bf22b60bb613b38fa709901458e`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10d384b97779774109c8339df3bd6d6f2ffad4242bf10bd7ff32806442654b3`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad94d4d1dc40669416aca412d7afde40639919f9d4814f225a46446b3e93f404`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38407276eceb8594c03684c6358996b55947d883d32bff640bc435d0d0b439`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96363b0a094772c0ae15f9f3f4991c52f15ae87fc8dcfe1274ccc1f97645e0ba`  
		Last Modified: Tue, 18 Nov 2025 12:59:49 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:3d7cc40ee7ce57cc7afc48ef305e0f3d897581d7e2f9ab9e3876635d727bd886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2863684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5237c858b06e8baba3bcc7235cb005847deea7f61ad850392dab0bb8261c0da`

```dockerfile
```

-	Layers:
	-	`sha256:0354bb9300ea32ab1706200fc61f1dbb8b24306851d68591ef7ae04ae3dddea5`  
		Last Modified: Tue, 18 Nov 2025 15:51:53 GMT  
		Size: 2.8 MB (2829062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b930ca1133f0600dc162ae497f32a81ed17457068768d5883a46d70bd00cf7`  
		Last Modified: Tue, 18 Nov 2025 15:51:54 GMT  
		Size: 34.6 KB (34622 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:trixie` - linux; s390x

```console
$ docker pull nginx@sha256:b23a59d3279511f84916907dedd1d46c0453b7c374c48e80c257165e908e9021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56970728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d845001c1a64267d0d697edbb31811c41b9700ef2934d0383896bb64e9157404`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:37:42 GMT
ENV NGINX_VERSION=1.29.3
# Mon, 08 Dec 2025 22:37:42 GMT
ENV NJS_VERSION=0.9.4
# Mon, 08 Dec 2025 22:37:42 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:42 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:42 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 08 Dec 2025 22:37:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:43 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:37:43 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:37:43 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f813d7fa207225672c9e9a722112545473254f43d458dfc8d2f5eed59a8a62ed`  
		Last Modified: Mon, 08 Dec 2025 22:38:05 GMT  
		Size: 27.1 MB (27131728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a1eb83d38136f08f04a87b85cc098dce7c9b96f653e260bc196ed2a7d5cbeb`  
		Last Modified: Mon, 08 Dec 2025 22:38:02 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb8b3e0f130a167c23d2ed7bd7a8ae6ab0b68f0e90c55b43c468e0d899b524`  
		Last Modified: Mon, 08 Dec 2025 22:38:01 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce2bfd07b6b9f33ddbde3f328b27ebb0e1b0d107832d4b55481fcef969b19ab`  
		Last Modified: Mon, 08 Dec 2025 22:38:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07051b34d36bbe897539bc449e608a27aba3ab08115677aa611c2490f267fa62`  
		Last Modified: Mon, 08 Dec 2025 22:38:01 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6324ac4d372abe2037de4d8d2fc53b99ef1d1e4d91ad3bbb7586330cca878`  
		Last Modified: Mon, 08 Dec 2025 22:38:01 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:9f1e20e0d6b347b04099f49f7eb3f7e3afd34b7a57541b2282e72380adc55f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2779575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b321561e51b11d87c0526337019f2b84ad52d26c27d791c18aa67ed9b0b20b70`

```dockerfile
```

-	Layers:
	-	`sha256:01a9d8780bd5fb1aa2ba5ad10b3aa3ca9eecf694ba1d89140f8fca551fa37082`  
		Last Modified: Tue, 09 Dec 2025 00:51:42 GMT  
		Size: 2.7 MB (2745031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4915786e5959bd7eaecfcea47dd4c9780cefb3c2d3e711e9ec007bac6389a4b`  
		Last Modified: Tue, 09 Dec 2025 00:51:43 GMT  
		Size: 34.5 KB (34544 bytes)  
		MIME: application/vnd.in-toto+json
