## `nginx:stable-bookworm`

```console
$ docker pull nginx@sha256:552e7481ca93ffccd046aa658dbbed22caefbc09c66fa7cd247cbb90b8a5c609
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

### `nginx:stable-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:3b03dfd827515a07ccf4946000f0bbdd2a4fb6aca7499249fcb6b1f9726823d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72386426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e04bb6b4bb37d45845842374be0cd181723daffb230849b1984aaeaa96faba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:39:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:39:08 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:39:08 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:39:08 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:08 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:39:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:39:09 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:39:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049fab013ee9578efd1a2b852e929746604a84227cac41598ba83c36691a180a`  
		Last Modified: Mon, 08 Dec 2025 22:39:31 GMT  
		Size: 44.2 MB (44153412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0da823c3c67d772bb4a4d32cf0297d7feb2e289ef7f3e02eb5564d7a636bc9`  
		Last Modified: Mon, 08 Dec 2025 22:39:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92ea34e4fd27efdcc15618de9871d33ddce300d74f45b06e72503b384cef0b7`  
		Last Modified: Mon, 08 Dec 2025 22:39:31 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cafe4fb0f5097aa7320bba842a1df5e683410392732066de0f6de9ba6670b2`  
		Last Modified: Mon, 08 Dec 2025 22:39:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a6b624459838cc90bc7303dd433ee069a77ae8dd787258ea6dff2278c885b`  
		Last Modified: Mon, 08 Dec 2025 22:39:27 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aec91fa40af2ca57c358a3436e8fa2dc48a8b3ed015eb3b5d61ddc9cf086374`  
		Last Modified: Mon, 08 Dec 2025 22:39:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:d7a2abcaa14ba0fe6ca46365a97276875d42335eccc6731fb684b4a032ba9264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831a6a5916f08607f0b2aa216006f874349f083364cb8540151d5934e05fb8a0`

```dockerfile
```

-	Layers:
	-	`sha256:8b2ed7576bb704f4a0db00c894bb0d8be501e7e4e00354ee0df907fc4c48f33f`  
		Last Modified: Tue, 09 Dec 2025 00:51:59 GMT  
		Size: 3.1 MB (3108197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27183f607c19447120388a402337503121ff4bb5c5bb32fab0ebc54b81737416`  
		Last Modified: Tue, 09 Dec 2025 00:52:00 GMT  
		Size: 33.4 KB (33370 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:c7a781f7524db7401db4b6f426600d5bdcdda847237f42ad93a9f4632b7df2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62447198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a5e4512b9884b02309fa1a6932331a7f77530a67da3ebdb133f1c1bf3b99b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:39:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:39:37 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:39:37 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:39:37 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:37 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:37 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:39:37 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:39:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:39:37 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:39:37 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:39:37 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f673e62470e3135aa81209765dc70bbc05bb0c0e289dc0547bb548d2e44fb3c3`  
		Last Modified: Mon, 08 Dec 2025 22:40:00 GMT  
		Size: 36.7 MB (36685012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04637fdc189b22db5f8983cf0d289d86b52f146052cefa3b670db5639cc19cde`  
		Last Modified: Mon, 08 Dec 2025 22:39:56 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d5baf5a5844f068803e3c61930efac95e235163e5ff071ca5a58f0ee21dc6`  
		Last Modified: Mon, 08 Dec 2025 22:39:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0edd39a13a1635a5e40098a1ac07e21884b77503736664859c2ab90ff593329`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7168cd2ffb4211456acc4abbb88305c2127bfb5c5eabc457abfeb3480d0640`  
		Last Modified: Mon, 08 Dec 2025 23:23:54 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eeb1d69906530ee4ea3bb71bc79c536e024cfa0ced225ef82645f6749ff908`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:2f15b8f701d5fbc49579793456afcedd2da35fd5703b99de8d153abfe1e15929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e7dc6c71c61cd587dc80b44773c896171e6fecfd3485ae82ef26e6b2a1ccea`

```dockerfile
```

-	Layers:
	-	`sha256:5c012df7511086207b350b27bff963b46ed8cd97c6a58e0a4027ed0b575a2110`  
		Last Modified: Tue, 09 Dec 2025 00:52:04 GMT  
		Size: 3.1 MB (3132209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112e7d9b6604b87273d5993fbd0140702b372f2b39443256f6f1f311dbfe0eb3`  
		Last Modified: Tue, 09 Dec 2025 00:52:05 GMT  
		Size: 33.5 KB (33466 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:fd432c8561d1f49b313fffd50e07e7a72a62044afae455df07983c49938d8b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60844167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d634def6966ff87d20e00e18be2eda30b450824b4c602605e410e00769b7af9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:44:58 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:44:58 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:44:58 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:44:58 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:44:58 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:44:58 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:44:58 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:44:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:44:59 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:44:59 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:44:59 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:44:59 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:44:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:44:59 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:44:59 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:44:59 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d6c050e5b4b3db9d4f406692d67fba18b8c10f2457ad492db7877b7b11a4f4`  
		Last Modified: Mon, 08 Dec 2025 22:45:18 GMT  
		Size: 36.9 MB (36905544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289d5f44d31ac99f7b431481da9da296143422317d78fc03a18a10f034cf984`  
		Last Modified: Mon, 08 Dec 2025 22:45:16 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96eb3198ceb330f012b8d813604216228d5a04b5ccf1be5a1a8cb80917042359`  
		Last Modified: Mon, 08 Dec 2025 22:45:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53d0ab2c13ed9e2f35343a6865c935d933fb6917784c6eb63b17edac93e6e16`  
		Last Modified: Mon, 08 Dec 2025 22:45:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f97e773e848476017338617fa88f728f2a888eaebee4bbc9359b6215bc81e`  
		Last Modified: Mon, 08 Dec 2025 22:45:16 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce7f413e18aae64d33d10bad5b58f4711d0debc9b01cd062fb864e4072850b3`  
		Last Modified: Mon, 08 Dec 2025 22:45:16 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:f84de2d565b9dbea4231b1aa3d0526449ed69919d3bf3e071e1d3acbe64f209a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb2fd100920cc1791635e63b167c40c8be4edfe55201cfb8dd6f149e31ac2ef`

```dockerfile
```

-	Layers:
	-	`sha256:59764ff4ab75435ba9397d3fb6f65bb1f1fabb5cab63f67621c32e0913eef7b7`  
		Last Modified: Tue, 09 Dec 2025 00:52:09 GMT  
		Size: 3.1 MB (3130868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616073da86e6a7a88f75f3284630318154607fb21bbe922f9ba29cd5305872fc`  
		Last Modified: Tue, 09 Dec 2025 00:52:09 GMT  
		Size: 33.5 KB (33466 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:b869934f513dcd08fc9de959e0bf6175e47ff3553a9c127afce9969722304356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68898682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf3298f4d8758381db6c085c4dc9963183b33da22b2baf25a0d1f94da4a918`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:38:42 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:38:42 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:38:42 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:42 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:42 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:38:42 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:42 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:43 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:43 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:38:43 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:38:43 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:38:43 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65205a1ec0e998ff66867c3ea7e2d51e876a5b5a6139e4120e53619e1dd5ec0a`  
		Last Modified: Mon, 08 Dec 2025 22:39:10 GMT  
		Size: 40.8 MB (40791860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53652562f6a510c2511a13f6bd2a67f4864d73369d0ff50554b580e48134367a`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43616d61949f51c9aec316342f158f93bea7d16a3675202243e3a45dedeccdfa`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a62e09e5a71ee7d320a5e47a4104c245f3ea44b2ff6e73ac58da49060500bef`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd55aefbf9bc823848558440dc31fe9789e2478ca6970308c0c28a194ed0a5c`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f6e1b1004a17efea5eb76046ed01b9b3c5dc51933d132469c25441fb819548`  
		Last Modified: Mon, 08 Dec 2025 22:38:59 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:a801904ea6e209e593dcf1a5f7950ecbbf0f529da10985fb5047b3a5e0e1848a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6208a2a9c1c7be68cb1ac01c1a441a1ed3b21fdd56d0b713db191cf005c011`

```dockerfile
```

-	Layers:
	-	`sha256:8d92ed272282fbefeaac38908912f2f217ebd2140a4acc33ce8c5183c350525b`  
		Last Modified: Tue, 09 Dec 2025 00:52:33 GMT  
		Size: 3.1 MB (3108600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce27445e6743c516da9b5015bfcb7e3862c19a3b553a63115780a2953dcce17`  
		Last Modified: Tue, 09 Dec 2025 00:52:33 GMT  
		Size: 33.5 KB (33497 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:e081c7cf868616c468395fe5df8e39cf75d83daa19ae97659aaee8845ae0b523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70778517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82e62ce80a4d9131aca0ae60443c5ebbde9bdc2e82b67840d42b1788b877ca8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:37:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:37:04 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:37:04 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:37:04 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:37:04 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:37:04 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:37:04 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:37:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:04 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:37:04 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:37:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cbd1e611cb6a84663f229c0a65b25b6c9b972853b83a76db43c6d7750fa3ca`  
		Last Modified: Mon, 08 Dec 2025 22:37:30 GMT  
		Size: 41.6 MB (41564193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0dffaf25ce9b3bc5266268c1ffa1c35e0b613d34d5ea822f57b0cacd6741e`  
		Last Modified: Mon, 08 Dec 2025 22:37:22 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578ecb0409903f24c01fed6d1714bb95d9d0be0ec5f84734d3d67a1a8f15fac8`  
		Last Modified: Mon, 08 Dec 2025 22:37:25 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b671c1db53793b862842554a55217fc8fa5a60e3c17c586cb1dfc7c43e3902a`  
		Last Modified: Mon, 08 Dec 2025 22:37:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c201614551bc1ff48ca6ab452751b88d0181f0b840c5cdb5b721f7cacf1404`  
		Last Modified: Mon, 08 Dec 2025 22:37:22 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d063eb07df0fae0348af9ce2c4ae7a103998324f62167f422f48e172e4a5fcac`  
		Last Modified: Mon, 08 Dec 2025 22:37:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:829e565ba62b4d1bfe4462b4d8db70501feac35f5df1dbbfcbb3a772488f5ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9128a253a183ba53f6fbf6a86ca2f0ed29bfdd86446881da9232621f85281707`

```dockerfile
```

-	Layers:
	-	`sha256:9a6be0ccca59ee24f5a18d4160e4205de446d9c2d88a9455e78e0ad924177e5f`  
		Last Modified: Tue, 09 Dec 2025 00:52:37 GMT  
		Size: 3.1 MB (3124088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49dda722bb59aac36e3fb40b32735cd09290cfe7167282c84fa11bdbf0a00bc`  
		Last Modified: Tue, 09 Dec 2025 00:52:39 GMT  
		Size: 33.3 KB (33328 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:7d99d4297deebf51feaa4899dc464ac8511688f7bf5469f5da35aafae9917f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68480372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ca760b04e99ad0385c22034082f53f9874bacb4f8b6715f9805e20fdd0288d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:55:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:55:48 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:55:48 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:55:48 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:55:48 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:55:48 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:55:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:55:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:55:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:55:52 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:55:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:55:55 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:55:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:55:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:55:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:55:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c36c6cee5841b41e7e41486782291dd0011ff928c80bf35c8feb80e57334fc`  
		Last Modified: Mon, 08 Dec 2025 22:56:57 GMT  
		Size: 40.0 MB (39961968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484b2a5c310224fe180a1e5127826b48a7d574f83c33009f435bc20902500d3`  
		Last Modified: Mon, 08 Dec 2025 22:56:54 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a81d643ece0b992b016d778be3aabdb3402551d3796514d5fb95a31ae13fe`  
		Last Modified: Mon, 08 Dec 2025 22:56:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db76af1718fe8fcd5be5989ecb629f7c1b975f0cf09fec138eac73daba29de4a`  
		Last Modified: Mon, 08 Dec 2025 22:56:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75c351a422aaa647798e8b1c30cc3cd4975bbab05d3add1bbb7f9591c71adb2`  
		Last Modified: Mon, 08 Dec 2025 22:56:55 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb0c4e60c0b6c97ed62a18143a3a9d1bf78d2292c33a80c21ad9646749aced`  
		Last Modified: Mon, 08 Dec 2025 22:56:55 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:1d44e69d2511891d32f1d4b98953150e9cd8f1a89dd9423ea27a8991026ae1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd928928c28c3f50c0e4d6744dff35d038d8a4988e77e2ac97a61475602af1c`

```dockerfile
```

-	Layers:
	-	`sha256:48ab294713e5440c718d7ad796194f50105e18d919c78a44281872d6065c15bf`  
		Last Modified: Tue, 09 Dec 2025 00:52:43 GMT  
		Size: 33.2 KB (33239 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:751cbd0622d08fff083851a2c4a8a944429598119932b8c795a30c721920aeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77113044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8af6f17812a850e3072b4464526e8887b8f9c711afe05f892ad2cd2c78a8116`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 12:52:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 12:52:33 GMT
ENV NGINX_VERSION=1.28.0
# Tue, 09 Dec 2025 12:52:33 GMT
ENV NJS_VERSION=0.8.10
# Tue, 09 Dec 2025 12:52:33 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 09 Dec 2025 12:52:33 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 09 Dec 2025 12:52:33 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 09 Dec 2025 12:52:33 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 12:52:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 12:52:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 12:52:34 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 12:52:34 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 12:52:34 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 12:52:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 12:52:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 12:52:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 12:52:34 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46da4c5dcfb65ac16d665b01a7258dc70d957097f5cdf4deae7f4016c8a0787`  
		Last Modified: Tue, 09 Dec 2025 12:53:33 GMT  
		Size: 45.0 MB (45039599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1f6f51348cb9223f7229699857886d05f1ac79df4c098f063c2e104e1b559f`  
		Last Modified: Tue, 09 Dec 2025 12:53:21 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e6570895ac02498fe3ee0cef4b04771500e7984384f4a271349364514994cd`  
		Last Modified: Tue, 09 Dec 2025 12:53:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ea8f5fd628731fec7a4d530bbd2b1a13652fb1decb6c6f750bb97f6b0fb7a2`  
		Last Modified: Tue, 09 Dec 2025 12:53:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db79d56533f9617bbbd3ab578eefd637007bb480757cc0ab19db42c8819cc9`  
		Last Modified: Tue, 09 Dec 2025 12:53:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c471b2c8746ac49fc16bc8a9d24efbc84ba5f314de6653c4499075241a1a46`  
		Last Modified: Tue, 09 Dec 2025 12:53:21 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:2698377e87fdd17e803cb4d59f93444aacc1edd072fd243305e4adb07fbdcbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61c4f7180a7777ca82f3708e09b3e6fbedd536b8d89cce6dda8be4663ec3d99`

```dockerfile
```

-	Layers:
	-	`sha256:6ee0eacc17bb914b3aed6f8ae76cbf5742cea28580a51ce7e5cb97c8d5d0849b`  
		Last Modified: Tue, 09 Dec 2025 15:50:54 GMT  
		Size: 3.1 MB (3138945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df0b3a288d2f3b19106bf3ccc1ee868180a580da4508e2756633c488bebff07`  
		Last Modified: Tue, 09 Dec 2025 15:50:55 GMT  
		Size: 33.4 KB (33426 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:16acaae086da9ccc679d1ef3814d562a732dc11b65e0d4884cf85a993621e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67104186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3d6dc920ed445302e60a383b0d7ccc2e11946e0575f7f37a52012ab671b14a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:38:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 08 Dec 2025 22:38:49 GMT
ENV NGINX_VERSION=1.28.0
# Mon, 08 Dec 2025 22:38:49 GMT
ENV NJS_VERSION=0.8.10
# Mon, 08 Dec 2025 22:38:49 GMT
ENV NJS_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:49 GMT
ENV PKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Mon, 08 Dec 2025 22:38:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 08 Dec 2025 22:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:38:49 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:38:49 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:38:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae825f45eb9b2203af3e170b3c78c1e4cef0e2488a04e42bff32930a2e01b5af`  
		Last Modified: Mon, 08 Dec 2025 22:39:15 GMT  
		Size: 40.2 MB (40215163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc595bfe91b7d227fb9ce7b1b1b684c72ed878269897e6702b32cf5829cd3f`  
		Last Modified: Mon, 08 Dec 2025 22:39:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8892b3d1b77b7f4e3a87f0d65f1191c8c35a6f8e046cc5adbafc00fd4333c86d`  
		Last Modified: Mon, 08 Dec 2025 22:39:11 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de913f5b83ad0c422cc0902edbcba5087b74efd0151ed16c12e5d83302bae4`  
		Last Modified: Mon, 08 Dec 2025 22:39:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea692534c73aca856735f5797a5d27c37f2ef351b8e6ab38e7a66a08ec48fbf4`  
		Last Modified: Mon, 08 Dec 2025 22:39:11 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1e4166082808c6f161c19bd98115e9801f06cce005088c71a86d55a27b8ea3`  
		Last Modified: Mon, 08 Dec 2025 22:39:12 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:30d8a12c2b1fc673a83596cc9c587caccf56f74a3a341482b30388778c5f6e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b0628f22c2e50aea3d93a9e2968af6b0ea55875246c2d04ec2de5869766b63`

```dockerfile
```

-	Layers:
	-	`sha256:278e4a2688e223755ae3e4e909b5e731d3a739445d189998045f508a47899d04`  
		Last Modified: Tue, 09 Dec 2025 00:52:49 GMT  
		Size: 3.1 MB (3118921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d354ff1323ae2dec93e7c93e2e177d1e15e2bf704decdd0e455549fa871642bb`  
		Last Modified: Tue, 09 Dec 2025 00:52:50 GMT  
		Size: 33.4 KB (33370 bytes)  
		MIME: application/vnd.in-toto+json
