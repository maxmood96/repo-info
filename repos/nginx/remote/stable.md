## `nginx:stable`

```console
$ docker pull nginx@sha256:e7e2c41c74775ccfe88d07fa3d9ebc9e0d6ae5c755244bc525153b37e308f699
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

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:a3db5704231cfd2be4c8300392ae5b4bcc82b231e48b08fac18e734e7a64f123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59747283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880187ad005d40ea9e8e22186af6eb8bb5857f9f3acb317aef7e88df40546429`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:22:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:22:42 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:22:42 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:22:42 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:42 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:42 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:22:42 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:22:42 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11696ed710ce5ae84536ff97168b170203ab5f2555eb0509333343deef1b0718`  
		Last Modified: Mon, 29 Dec 2025 23:22:59 GMT  
		Size: 30.0 MB (29966149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02acfc0013cec4f759baf8827fbd1ee127586c52dac2fab38abddd67fd56983d`  
		Last Modified: Mon, 29 Dec 2025 23:22:57 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad526308e1f4fa50d5de1262873de498eb7653a5502b80006168afb9e66ac14`  
		Last Modified: Mon, 29 Dec 2025 23:23:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a728426e5c161f970763d97776d1477cd479d1e38e3bac4c973af23f0b6a329`  
		Last Modified: Mon, 29 Dec 2025 23:22:57 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bac657aeb9d5dbc318cc8a05a3296bba89b6d93382adbe958266feaf2d6bfb`  
		Last Modified: Mon, 29 Dec 2025 23:22:57 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60406108e59d54d9b826325722738f28476d9f1d308a9d81a3ec4e8dc702b9`  
		Last Modified: Mon, 29 Dec 2025 23:22:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:a3fcf6cac79f0b2f8cb6d208352dd427550b6766309998dd190bf2392e18f99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2843926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a354708bc06af5a8f8daa32c7e4a1b140feb50037073001fad2992680fd4fd`

```dockerfile
```

-	Layers:
	-	`sha256:e14de928287b115ac695d08e09bee028a24bd0aad92afad7471bd98ffb59fc8e`  
		Last Modified: Tue, 30 Dec 2025 03:51:57 GMT  
		Size: 2.8 MB (2810595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8129c0b1b94b479314e2b67e48d63cd12c0f9eeb9cf1fdd74cee42e253e75233`  
		Last Modified: Tue, 30 Dec 2025 03:51:58 GMT  
		Size: 33.3 KB (33331 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:17401ac7f503c54e236a5cc9b03c694e62f61e245f4dc4a893665795a2e0aca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51354987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861ec8b1559bd4c40e4a8aa3966e2cbfeae972447edf88b0143858e62efefc6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:55 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:23:55 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:23:55 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:23:55 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:55 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:55 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:55 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:23:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:23:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:23:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4defa74e7bc26e8dd6038578331adf26eff7b163e080d787e64c63730f3518c0`  
		Last Modified: Mon, 29 Dec 2025 23:24:16 GMT  
		Size: 23.4 MB (23406243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc6547c6ff89abaa6447df476e59eb1ac36cabc6ba3b71a34ea7a47983ecf57`  
		Last Modified: Mon, 29 Dec 2025 23:24:12 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d0039f15ec08db143e59010a0f306ad2ae621d704165961d4d849c773141b6`  
		Last Modified: Mon, 29 Dec 2025 23:24:12 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6214a2de82e6563bacc8245f4b858ac10170e98224ca09271217dfb8df74d86`  
		Last Modified: Mon, 29 Dec 2025 23:24:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0f1d3138f3b4c0ac177727e8c1192c3a89933d78cd8530ea7414a9d587f7e5`  
		Last Modified: Mon, 29 Dec 2025 23:24:12 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63bf5e25979bde1502440e00baa8e8e57f9648c2908afc0b1cd6f55984c3ade`  
		Last Modified: Mon, 29 Dec 2025 23:24:12 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:674246474ff8f1338375d9cb35b750705496112b817f330655fdbe7c2ee6ef45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76703266f1a2abda7b8aadbf7a259621ae75a6e3c63eee7f9e07f474f8ae6f`

```dockerfile
```

-	Layers:
	-	`sha256:ab8cf481b1cf76b8b449b3ef3690aae3ff9331a8d5e1d4854257083343c3a541`  
		Last Modified: Tue, 30 Dec 2025 00:51:50 GMT  
		Size: 2.8 MB (2836703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb12c6774c68579312d128e4a76c93d75e8f3caa83cddbef3100653beec9e89`  
		Last Modified: Tue, 30 Dec 2025 00:51:50 GMT  
		Size: 33.4 KB (33427 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:491c81b725998165c0c44f79c454f9e3615fc63dd6b60ea0088d7b168ed13b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49623986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67414b56810ea993b7b05d8782fa727a402dc6bb8746c53d801df7f14292c8eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:23:04 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:23:04 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:23:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d36e52d6ce95561cfe9c6f99dcc6f9b240ac29b409bfda49b4b3c48d1654e1`  
		Last Modified: Mon, 29 Dec 2025 23:23:24 GMT  
		Size: 23.4 MB (23409387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8c9290bf66350d025eec9a3a68d8ae4bb0846538115a5b61cee00b4883ee9`  
		Last Modified: Mon, 29 Dec 2025 23:23:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1793f9dd176ce52ec5d24a1fb1dd197397438acd6ee8cf32fdd057b4c5dbb7`  
		Last Modified: Mon, 29 Dec 2025 23:23:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce4b0702c80f67e1caa4823f6a4aff2b43b8a5646f7db930ae81ff6535c286b`  
		Last Modified: Mon, 29 Dec 2025 23:23:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9efe87199cbb0cf8a51d6e9b145cd20e9d45772d29dcd639be3724150a5e40`  
		Last Modified: Mon, 29 Dec 2025 23:23:20 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38754f413ce22b20c14d668cea4d074e56ffd9c37033bfe8bad2cf84390c39e5`  
		Last Modified: Mon, 29 Dec 2025 23:23:20 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:909e30422791d0d4446445aca78d5c86f293d35bb10ea5d4cbcaaf6bb4ba3f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dcae5891a0ecf149273ccd04835428307e33e81149e30466269dec5c9b9f17`

```dockerfile
```

-	Layers:
	-	`sha256:ca08faddae8019149d5544c6944fa4e090f044494120e7bd1213a0e8cd5626f6`  
		Last Modified: Tue, 30 Dec 2025 03:52:04 GMT  
		Size: 2.8 MB (2835448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb124ca74dbf851f5f65622c1ff5b911102cc0669b6cad82f1dc3f5290c22d7a`  
		Last Modified: Tue, 30 Dec 2025 03:52:05 GMT  
		Size: 33.4 KB (33427 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:aaa9b5290e6b5996bb00301c1f33d04038e875d8aa448f5ff9067b9e1f1a7c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccff17c89f8cc17cc61655bc19426285fe5c5f91e0389ae20af542c8deb5fac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:22:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:22:30 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:22:30 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:22:30 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:30 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:22:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:22:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:22:30 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:22:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9144c6fbf7afce7ffd1ab7db96d3397477b9625ae718aa5f56c0af1048df8d`  
		Last Modified: Mon, 29 Dec 2025 23:22:48 GMT  
		Size: 28.1 MB (28094328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4ab0189cd22766f41166a126d80aa65278f830c2ff5eda657b3a09b7c3df32`  
		Last Modified: Mon, 29 Dec 2025 23:22:47 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e2bfe48432841a2cd2390bf1b23d50a2973c52cdaf1d3a460f16485172b473`  
		Last Modified: Mon, 29 Dec 2025 23:22:46 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a381311e11d7d0ce1e2b3d9bf56ef349a153d6f26084813692930cd2c50fc`  
		Last Modified: Mon, 29 Dec 2025 23:22:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684615d7246f776df771a2507fe8ac3af30cb0df129b21234c3628fda1f1e154`  
		Last Modified: Mon, 29 Dec 2025 23:22:51 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972880a9e9506605583fbcb7efc5a0bc6932cdcefcaf4c2f640bcccfb4860dc0`  
		Last Modified: Mon, 29 Dec 2025 23:22:46 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:210915052bde8149d102d52b5d76bde07142a9442489d9e37148af21a5254e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837cc8bb389d7277536f57f3d7b4a24f3261e788b44765a49b30703acf720858`

```dockerfile
```

-	Layers:
	-	`sha256:6e8422ccfffbc04e071da16a0caa0797e77f2286f1a21c3f79eb6fc21d649ae8`  
		Last Modified: Tue, 30 Dec 2025 03:52:09 GMT  
		Size: 2.8 MB (2811031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceeef3973975bd2209ec27a4d16d8eb4ec66fd24163aa1e139e4e01345f2184c`  
		Last Modified: Tue, 30 Dec 2025 03:52:10 GMT  
		Size: 33.5 KB (33457 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:ada9abd2262aee89124d794aec7d787ec3344ba0650d8d047aba74f38d80dca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59985529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339aac1bdb07e14dc5df4887e77e099e56b07fe0b4a8f2e64fca12d3f4fe2d08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:13 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:21:13 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:21:13 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:21:13 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:13 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:13 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:21:13 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:21:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:21:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:21:13 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:21:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d715da7e4f40ee90ae4cbc4d8894dfe730f1070a5d9ef7208a91a1e0c17e1fd2`  
		Last Modified: Mon, 29 Dec 2025 23:21:33 GMT  
		Size: 28.7 MB (28687828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2cf70fed1033c2cf1b92b969c16bd64ffe216e05075762ead96dd39001ace5`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae02154642ea076f724a3b3fc93c25db4f3799ee80231ea5e5577f576cd9c4`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6def1923e0419e86ad12452d8880e66980cb1182be1fbeb85b37b1d61e0b9f1d`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c768979953cf25220c5bd6c001563b84fc0903db59cdb93720afb2ec3deb508`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95b440631182df05a16e98e4c5a8b3aeab5d7c34e611ae2652ab503dd7afd3`  
		Last Modified: Mon, 29 Dec 2025 23:21:30 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:4045493ec816f5af8379d5237e1fac8390a9a9edd25489ebf6f2daead4eaf1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2863740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edfcc77dde36b27cb0288d5aa372467166d7ee350ab849d5f625d7ce99ee520`

```dockerfile
```

-	Layers:
	-	`sha256:49475bb75b71a8ee43e1820af413595f965785f14000bf4f42cba150315fce98`  
		Last Modified: Tue, 30 Dec 2025 03:52:14 GMT  
		Size: 2.8 MB (2830451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc82a32b5f800b6638203ffc581227fa20e10fa809df92e8cf09e6cf122769c6`  
		Last Modified: Tue, 30 Dec 2025 03:52:14 GMT  
		Size: 33.3 KB (33289 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:0b05f7338a77415952400b86d547c49e7aa2558d85f003f90809edb20c47fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63815323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458fb3bb428bee1d4d09fefd517c18cd7464774f32b992c95b7067310f08f167`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 16:36:00 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 30 Dec 2025 16:36:00 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 30 Dec 2025 16:36:00 GMT
ENV NJS_VERSION=0.9.4
# Tue, 30 Dec 2025 16:36:00 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 30 Dec 2025 16:36:00 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 16:36:00 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 16:36:00 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 16:36:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 30 Dec 2025 16:36:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 16:36:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 16:36:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 16:36:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 16:36:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 16:36:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 30 Dec 2025 16:36:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 16:36:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c40f77f3097aa2b6dea736b78e61f02488776faec2c34a49812e9299348c69`  
		Last Modified: Tue, 30 Dec 2025 16:36:38 GMT  
		Size: 30.2 MB (30213828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9d7335c7b7ee629b596ac4f478f17df4a32c9ad9bb24793ba726eba1fbd34`  
		Last Modified: Tue, 30 Dec 2025 16:36:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574ff1c2dfeb55c06c99dce3e91875f55b1dc7edd956dade83905e7be3f9d06`  
		Last Modified: Tue, 30 Dec 2025 16:36:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e1087ff4744781e2badd8ba914d0fc5204ea55c8f978407749162c8f6f426`  
		Last Modified: Tue, 30 Dec 2025 16:36:32 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef07501716da9bd75edfb74279fe95cd8f68e7779212d404037e5dac4278ee`  
		Last Modified: Tue, 30 Dec 2025 16:36:32 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec0d6d5e1084410f6cac28b19909115a423d22ea3ff83166a4ecd4d92e9be89`  
		Last Modified: Tue, 30 Dec 2025 16:36:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:ff3f564b4007efbe9d2001f4c0dbf1a0e54cec482bb8f32631b5d0adefd2aa12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eec4de01a5a32b733ddd844fa10b005292937de5776858cee7e7b0e94def96`

```dockerfile
```

-	Layers:
	-	`sha256:d0db16bc6cea1ad2f057327541e6b77cd594fd39713dc3f893d9c0c59f12c5cc`  
		Last Modified: Tue, 30 Dec 2025 18:50:59 GMT  
		Size: 2.8 MB (2838101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f847efda4f294d81abb2d551bc2bd2020bcef55583d7daccee740a8bb655d6f`  
		Last Modified: Tue, 30 Dec 2025 18:51:00 GMT  
		Size: 33.4 KB (33387 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; riscv64

```console
$ docker pull nginx@sha256:4a4e5b223eea4713ba88d7a8a7c80c20cf23496fbb3e4ee36e59ebe19a284be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54680875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071369d881f33b552c56cdda55e1f8a1664ca170a47c75e804739c488751cbf2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:13:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NJS_VERSION=0.9.4
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 08:13:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 30 Dec 2025 08:13:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 08:13:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb01b00c6a6116152fa50d416897aa6976c014d4b0cb5f7a3f7f61aefbd8e4`  
		Last Modified: Tue, 30 Dec 2025 08:15:01 GMT  
		Size: 26.4 MB (26403135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69004e499cb8b74bf07a31b6fcafc1a95ae6600653bb84b5fd24f23b8584ed38`  
		Last Modified: Wed, 24 Dec 2025 10:24:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40556089a349428f49a73b68585f186724f7e9bb3600157b55a58b5399f9aa57`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2342f66cb613c38fdc6e1b35b9085e4d0be036bf2beed2e64800eeb702c7b99b`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaa6d933cae498ce1e55ae815ff971b9b6adc01d7d2875dde2cc55e5c2cae44`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a30a5475ac828a97d58493ecfb54de35ed14032cfaef262ae9bfd0864c63c5`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:1d00db3ab39a123a60b3b3bbb9ca6dd79198f46c1e2a49140228c7bcf1ccb201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2861275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008fa9db43ae0bce0527c80772532e0061a3c54eeeb4c415cab610631be635df`

```dockerfile
```

-	Layers:
	-	`sha256:de83e9266c1ed576dae353179bfa07f29e92ff96c0f47e9d20825d4649f9f0ca`  
		Last Modified: Tue, 30 Dec 2025 09:51:00 GMT  
		Size: 2.8 MB (2827888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f53f93b390c857a665fc90e3c2d9134f0261c97777fffe31573f7e8e09b78fd`  
		Last Modified: Tue, 30 Dec 2025 09:51:01 GMT  
		Size: 33.4 KB (33387 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:2619e02872ddd533345f43c167bf495830d80c1d75bc7416f33484f4c9a817dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56964901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00d560946c334610a283574fd5fcd9ba2f073760b296d69ba8d83b5b19f7fcd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NGINX_VERSION=1.28.1
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NJS_VERSION=0.9.4
# Mon, 29 Dec 2025 23:23:04 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 29 Dec 2025 23:23:04 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 29 Dec 2025 23:23:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:23:04 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:23:04 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:23:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b928b3ae01bd37579c17b3b9480d7d385f4e86f74790c8d1a9ea0d6946900`  
		Last Modified: Mon, 29 Dec 2025 23:23:27 GMT  
		Size: 27.1 MB (27125885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0719ac254b53a06d82661d3e9cead3710618cda4b50c4a5e2859b5408df598`  
		Last Modified: Mon, 29 Dec 2025 23:23:25 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df1ce9503908f03d9105452c5182998e10033775dfad1d9b63139ae987844f`  
		Last Modified: Mon, 29 Dec 2025 23:23:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3b360c4f05fa37de4b80df4f69db2296ce31fed9614495ef5d95af6f7fc8de`  
		Last Modified: Mon, 29 Dec 2025 23:23:25 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b479c1234afd73a06f845724fe115b53dabfc6c937d8f4d646bfdd005d489c`  
		Last Modified: Mon, 29 Dec 2025 23:23:25 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674447875f5449c8e100175351f49d16d5f9877166f9c21062dde34e66f04bc`  
		Last Modified: Mon, 29 Dec 2025 23:23:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:c055410076fe571607b87bbf3cd8e7638e95739d82490b0f9f5f82a3a3627af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2777211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484a9a8821a125e5001005c304cfcabaaefcde0e64e52b6f46b26755991e77a2`

```dockerfile
```

-	Layers:
	-	`sha256:f31348ead94b1454b27693f7720d0019c4cf6c47a1e45b53b108853aed1a0b20`  
		Last Modified: Tue, 30 Dec 2025 03:52:23 GMT  
		Size: 2.7 MB (2743881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce11411043850eb73e0436283eeb416c12a8ee170b6851acca3f84015003c07`  
		Last Modified: Tue, 30 Dec 2025 03:52:24 GMT  
		Size: 33.3 KB (33330 bytes)  
		MIME: application/vnd.in-toto+json
