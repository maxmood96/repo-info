## `nginx:stable-bookworm`

```console
$ docker pull nginx@sha256:d65a29796e52943c6acb610df9a338542e57b42b70ee0d82344daf03382a8c3f
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
$ docker pull nginx@sha256:d9c62df87ab2f884f401f81e170f2dd3f7e0b0ba6983a144cf73f2015698a13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72385516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0a563e3e6a4c41dcdb46a5c1db44dd74662631dd2d360b5a3e9f5ebdecaf27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7b49ada9e3e25725e6bc94a079613129c3b9d893d28b236931d2cad6fcf54e`  
		Last Modified: Mon, 29 Sep 2025 23:56:16 GMT  
		Size: 44.2 MB (44152585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5924dfa87c10568595db545b140d09e5e9be85ba21b8859587fcd373d31812`  
		Last Modified: Mon, 29 Sep 2025 23:56:11 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a18bc0c059852348f5e8d9c285e40d0b2004116487c916bb5a6f72430359e`  
		Last Modified: Mon, 29 Sep 2025 23:56:11 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be90cf255959ccf787bbc87202ccf21efaeb132f64649488eb5474f5f8512612`  
		Last Modified: Mon, 29 Sep 2025 23:56:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb62151b9daa7eac41779925674d3cde3cb829c3df42050a05687fe72f4ebe`  
		Last Modified: Mon, 29 Sep 2025 23:56:12 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4f638eff8b364cac5ae6044a641875d64f44e1f4558ed4791ae64c1e5cd16`  
		Last Modified: Mon, 29 Sep 2025 23:56:12 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:984b8241ad4bb7f9675c0eb0bdf6d499f3e4ba7a16832c90a7ab037ec366ad3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1efe045b836d8dc5abc90284e3d83af203a9414b40c16259147ef375e95e1fb`

```dockerfile
```

-	Layers:
	-	`sha256:e5f6a43e71f25cc45847548236316cb8d983b4530d036f1857160cf16c7f1ea5`  
		Last Modified: Tue, 30 Sep 2025 02:51:16 GMT  
		Size: 3.1 MB (3108197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7f78347f483ca9e18f53f264a8b41c1ad937c5835097113a32a17911d1a722`  
		Last Modified: Tue, 30 Sep 2025 02:51:17 GMT  
		Size: 33.4 KB (33412 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:5c42fbb194e66ce5acaa98ba6ea9851fc929575fec1cea23448ed0c490f497a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62447020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7ea7ad278aa9a79e08da0db6dc95339c5e39b6fcaf01f07b6167a28a48dabb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90696501da51c03577c993b767861011d74492425a25d089480868573c1cb9ed`  
		Last Modified: Tue, 30 Sep 2025 00:02:06 GMT  
		Size: 36.7 MB (36684984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8da45c8a4b416ef2ec68bb23317e0dedcec2e5e21bc7f905cf340ec97f3e5b`  
		Last Modified: Tue, 30 Sep 2025 00:02:02 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77d8dbefe59723ff40915f4139ff00ef3c20ed7b0719e2a64020f50f58c846`  
		Last Modified: Tue, 30 Sep 2025 00:02:02 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67d8e7bb649a8a333c80c015f395e063c7f0c97ea73ef10138e7d33efa1ff5e`  
		Last Modified: Tue, 30 Sep 2025 00:02:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f4009c66c0f1bd6c2e72de95eb7929155d10fe0db418f772a91d82fea0c7c5`  
		Last Modified: Tue, 30 Sep 2025 00:02:04 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a904a37698f542163aeee07493796140fadc7e05a6ba614dd71dc1837539f`  
		Last Modified: Tue, 30 Sep 2025 00:02:04 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:2e8b89822da138e39c7107864ed7c26bb3839acf37b711b9769998be57b3877f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79fc5418b5bb86d1974365dab1a5aaabdf20759dcbd3955ef52f1848f36ab6a`

```dockerfile
```

-	Layers:
	-	`sha256:9a94451c170693549bbf415c1da53bba119a34d0a9c04ee9da8de7364985e862`  
		Last Modified: Tue, 30 Sep 2025 02:51:22 GMT  
		Size: 3.1 MB (3132209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc1e738e5d8e30fed26f24de07467521db6d084325b1a935df806dc3f68eaeb`  
		Last Modified: Tue, 30 Sep 2025 02:51:23 GMT  
		Size: 33.5 KB (33509 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:f93b854d098e6105f36cf84d1744351505c08e0dc919bd47fa61198ba4980d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60844124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cddce5c3ce7c615abac96a583e12cb3db2207b013ce6b255b68c3921d04eb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf710c3da1d848530e8a074d6e249f2336f9c45fb30bf06c1a201b4200e54493`  
		Last Modified: Tue, 30 Sep 2025 00:04:16 GMT  
		Size: 36.9 MB (36905588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57417b80252e94c53f6fb1e2d7af54b3e521bce25bafd29ff82fe861a678fec5`  
		Last Modified: Tue, 30 Sep 2025 00:04:14 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91032cf19664963ee6ce29704e5a6738ed1e415b3d4f091bd591ad4f7515f3e0`  
		Last Modified: Tue, 30 Sep 2025 00:04:14 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd609c7cdfbb5778cceec0309805bf57807e2f65c74389f9bc0857811fba87`  
		Last Modified: Tue, 30 Sep 2025 00:04:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54adb05f91b289314eaf8ed52888a527dc6401214fa7193d3853a7cc22ad4cae`  
		Last Modified: Tue, 30 Sep 2025 00:04:14 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7422d6ae7fc7d792b74ac98851f64aa65b4add6e16353f2413b9a21f0c5c8408`  
		Last Modified: Tue, 30 Sep 2025 00:04:14 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:211c0908fa8dd4e2e376d3490481566b1c468d65c1941680273750792a2c10c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc23ad013f173b240bffe187ccd5625fd51744afbea9f867f2542525ff786bd`

```dockerfile
```

-	Layers:
	-	`sha256:fecedbeb3a70c28972473c0bc92a1497453834bbab99fde93ca4713c781c038b`  
		Last Modified: Tue, 30 Sep 2025 02:51:27 GMT  
		Size: 3.1 MB (3130868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca2363edbf5ca5968a0167acbb19b52aac5ad272dfeb755ba28705271bb72b0`  
		Last Modified: Tue, 30 Sep 2025 02:51:28 GMT  
		Size: 33.5 KB (33509 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:bb54ff37056503b27dcf3fc7c4a7aeb0b29373519353cc88248455b2706ecdcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68897190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e3942d93b7c9e68a5e902395859d4f53de5aa9a187cba800c72cee6f9cb03f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95ba757b4df15ebaf47a30437d48c187dda95e9bb33cd2cdda05c3e41bd5c1c`  
		Last Modified: Mon, 29 Sep 2025 23:56:25 GMT  
		Size: 40.8 MB (40790453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8f88bd2ef16c8cd0558ae34d6ec1762cdc7273079f87d542d399589b1f5225`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3354e7ea08f64dd7dd4179d47e7d7a2fa6c302657818c1e865dbd315d7d6bc`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde06bc0d11975d1a6b05087c82c9410678d3fe662858acc41ba26fd734acced`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebe3acca56c8fedf9e4438e72864e6a5e75b6d229096c8ae0f80c820e9a40cb`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df078daad3fe4ddd7507c23839c50d9f43bc99e23ec9fc45a86318b8080c1e`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:8f725cf1ea987a5f1e93b838490dfaae955ee897448f9a60e7f70b08c9d4ac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd05de4d2be0860d6230c01ec19a0a9075e5c2e4bf23a2681a2348defac661a`

```dockerfile
```

-	Layers:
	-	`sha256:6b72efac6fb1dc0eaec7f5b38a328d014add43b8d00aa1216d8680588aa6befe`  
		Last Modified: Tue, 30 Sep 2025 02:51:31 GMT  
		Size: 3.1 MB (3108600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5593555571617893af69f5ab8a4f0c5e247c5b7561c0f7ec858b09426b40f9`  
		Last Modified: Tue, 30 Sep 2025 02:51:32 GMT  
		Size: 33.5 KB (33541 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:65fa4b21b132808d912dce4978bc4b42c0ce66d7e73c90a75f79dfe3e6058c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70778105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7195e17b6a118dfc4955e5f53f8bed8230da6cd2630637f639d3778ee0f7a36c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772ebe2029fb062e962397549fca784eea0bacbe90ddff43ef839ac48c71441b`  
		Last Modified: Mon, 29 Sep 2025 23:54:25 GMT  
		Size: 41.6 MB (41563875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb1b1caf2f02bde428c70faddc4d7fea6fd8c14bee1728ccad5274b2cc74e25`  
		Last Modified: Mon, 29 Sep 2025 23:54:23 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e4bf3f5ab543a2f978a291c7fb2e0d56286201b67b898ec94541dcf26fc03e`  
		Last Modified: Mon, 29 Sep 2025 23:54:24 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c3777bb890acd76795e64ac8e239c7f543f9535bfd0024ee0f2db6d7a58137`  
		Last Modified: Mon, 29 Sep 2025 23:54:23 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6433ab64f85bbb97c51767fc93a5aadebbe40fb996ceff613de2047f0586672`  
		Last Modified: Mon, 29 Sep 2025 23:54:23 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22783d917311ffea3c010144c8f90bc473de8ab70fa1223a644d2edc4c5f85f6`  
		Last Modified: Mon, 29 Sep 2025 23:54:23 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:bb1145770e32717bb694e2ec5dd843c7c242d938adc419be5986397d0e294522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c30a0ac1206db7a1cf671b1e6390601f98aea1c8b392e2e6d7a6dc241f0608`

```dockerfile
```

-	Layers:
	-	`sha256:e7656be89381a2e435eef095aa8314c05f607e2547c040bb86ed2b2fafd1f195`  
		Last Modified: Tue, 30 Sep 2025 02:51:36 GMT  
		Size: 3.1 MB (3124088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67114899bfa4ce43cc7301c7180fb57e01ade3375a6cc8913b70464867b2b875`  
		Last Modified: Tue, 30 Sep 2025 02:51:37 GMT  
		Size: 33.4 KB (33371 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:e1656310775911b7e74a25d1a5209ae8edaae560162c03bdf4e3a0a226e22cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68480306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d135ef85a912510eb2fc0d129a105ad88f7d904404832dc273118602c1bb4017`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:67737a113ff8fe4461be953b475f1930d91e20d222e9a1f4e55ddb9bf4c2c6de`  
		Last Modified: Tue, 21 Oct 2025 00:19:57 GMT  
		Size: 28.5 MB (28513717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32781cd62ce852d02eb74a682c122fa3c8062ed8d4777cd8522a391eb8d38913`  
		Last Modified: Tue, 21 Oct 2025 01:45:01 GMT  
		Size: 40.0 MB (39961991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e9434608f94ced72a675dbe73728505713bda1fce510b447131ac0c07ceac9`  
		Last Modified: Tue, 21 Oct 2025 01:44:58 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6851b7b62dd3f0f9d15b41acfcd44b99b7ed9fa5a8127cc1bbeea079fd101e1f`  
		Last Modified: Tue, 21 Oct 2025 01:44:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c2bc2daa4345fc92bbdae66b5588a3aed6909259395ec4e470c87a6d05e560`  
		Last Modified: Tue, 21 Oct 2025 01:44:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce88670add77cbac142d3ba98d3d5d35aa165aec8338fbf52106f334b293817`  
		Last Modified: Tue, 21 Oct 2025 01:44:58 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ad791ba1d388680c6f5d80e1ec4eb78b15e7e601f2b408e37d934823d0c2ef`  
		Last Modified: Tue, 21 Oct 2025 01:44:58 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:3276b64dd63f143fb49e238bd206340f1e93e1d4552b2f316c644878a1fbc1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af792c49e308055cbbe00ffeedc96064a25b90c4b6dc488c5b2d03a7455f6ad`

```dockerfile
```

-	Layers:
	-	`sha256:0ba532d7d6e6a111faaf8d9651fffd1214fe38c5bb54480216dc1f36e0b87872`  
		Last Modified: Tue, 21 Oct 2025 05:53:03 GMT  
		Size: 33.3 KB (33282 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:30b09ac3de321b8f45965ac93d3bb819db52ce8b4da9e405efcf109254da0464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77112351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e4bcd8898d8613e85c31268342672b95c7f88cad6405852eea4f401d2313fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7851d644117ff3bc326738fa5598a593a3132a7f5cd32447494c4d0f92d7153`  
		Last Modified: Tue, 21 Oct 2025 02:11:32 GMT  
		Size: 45.0 MB (45038973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab3a518b30dc1d72e260a988e87fd983960e6091b09c81a4461fec5aec99d5`  
		Last Modified: Tue, 21 Oct 2025 02:11:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83786d39cab7f9b2eeb89aee823c8beddec8e55cf60acbb349bfb524a084c6`  
		Last Modified: Tue, 21 Oct 2025 02:11:28 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7f28615eee3eedd2386fe4d99c46af266df754c35ad3df73abfa0082b24ede`  
		Last Modified: Tue, 21 Oct 2025 02:11:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546c7fda4ecfab1c93a7e98cf1a4769febdba20bb0688995aadf3ec6d0f95b6`  
		Last Modified: Tue, 21 Oct 2025 02:11:28 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf041a9791e34e70620c8a1f7bd4ec805ebd8aab7a5db537d98ea45dec809dab`  
		Last Modified: Tue, 21 Oct 2025 02:11:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:42f819cece5d5e57cab937f6bb57dcdc5031a4c0dca08dd60fc1229e8efc3f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a05b027b95231a5d0b2048cf8af190384d6c723bc6e6052eb36de916428fb00`

```dockerfile
```

-	Layers:
	-	`sha256:45101560c48166a087c1b021b55d93014e40cd2af6117c570f3e288a52a94e06`  
		Last Modified: Tue, 21 Oct 2025 05:53:06 GMT  
		Size: 3.1 MB (3138945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0e80e0784628e33ee81040143e6ea9d2fa0147f0cab277a633e5ff1fd46d727`  
		Last Modified: Tue, 21 Oct 2025 05:53:07 GMT  
		Size: 33.5 KB (33469 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:ebc055898c8a6bdbe185bffe159d83b4274cbce38e146d427b2c5a46688a0c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67103288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d5d1eb7a02c2abd7c11baeeb23d7745588393a7fd2337d55651131101c02c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_VERSION=0.8.10
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9bd89af4d33acf0d647f2e2cc79735bd1b7e0fc8746dda280c915a8ab3e625`  
		Last Modified: Mon, 29 Sep 2025 23:59:07 GMT  
		Size: 40.2 MB (40214368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9937d007499d742e67ebdfbb90f283d3a272883b0ca0e8f49d002bae1d74f5a`  
		Last Modified: Mon, 29 Sep 2025 23:59:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272785894976dc94e25964cb48c1cf1f830218d543fdce0ba98fa9f6ccfb1615`  
		Last Modified: Mon, 29 Sep 2025 23:59:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48999e56c29bc54d25f192ce770dfd77a2ab818549a3eefd77ea12978c0e8487`  
		Last Modified: Mon, 29 Sep 2025 23:59:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34df17c8d67cef4025ef9a1e1e456349643c6c82ba2b523b316c1cf61c607b3`  
		Last Modified: Mon, 29 Sep 2025 23:59:04 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cf5241af437bc5c1c0f7a4d01eb64b6c0f017c2455376d9172034f77a60e06`  
		Last Modified: Mon, 29 Sep 2025 23:59:04 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:0253dae5a1e633e5a6272b244bfc27ebbf70fce2aa5857ac03462e5060c4e06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c370e4b51dcbabe16e210f0d734309abec8d1b0e995d76fdd029053b4b10ab`

```dockerfile
```

-	Layers:
	-	`sha256:79e7e397bf2fb86502b7b0b0e8ced4c2227dfd4dd2894c1a257e2918c4416502`  
		Last Modified: Tue, 30 Sep 2025 02:51:46 GMT  
		Size: 3.1 MB (3118921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9902b4cc79853ff8e767ed20316919da4614fcad5005a343557aacda4e6a9037`  
		Last Modified: Tue, 30 Sep 2025 02:51:46 GMT  
		Size: 33.4 KB (33413 bytes)  
		MIME: application/vnd.in-toto+json
