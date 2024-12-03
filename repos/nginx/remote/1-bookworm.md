## `nginx:1-bookworm`

```console
$ docker pull nginx@sha256:fb197595ebe76b9c0c14ab68159fd3c08bd067ec62300583543f0ebda353b5be
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

### `nginx:1-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:3d696e8357051647b844d8c7cf4a0aa71e84379999a4f6af9b8ca1f7919ade42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72078352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f8bdd3810c96dc5c28aec39583af731b34a2cd99471530f53c8794ed5b423e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ee30bbe5efddbef9cc0245ba52b133d3c8897a6565faa6c5c87bc552b5305`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 43.8 MB (43842177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc1569e58f52d008e232130d8fca2411f417ea423305cd7d7b513fb96d22947`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f35df001b4bd6f8733cd4abe8e1493582782404fefc2393129a5dfb5e72df`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e320bf29cd3ef51b06a3dfe259b2582d48be27a9ac4c6b7af6fbb99429d210`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50399908e1c0958c409f3c844d61736fd41e37a58dca4832927715508dd3aa`  
		Last Modified: Tue, 03 Dec 2024 02:17:25 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b64962dd94d4818372adf30dc0e2ca4803c46d4f638b7712fe01a149c705c5`  
		Last Modified: Tue, 03 Dec 2024 02:17:25 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:04ead2bc6e759e8e81d5ccfffba09138b98466f4c98918cbea8c802e4718b4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2993719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f808fdfd7ec9b22646e9379b4618c4926dcfa8b820c08457c3bd805e90e3f1`

```dockerfile
```

-	Layers:
	-	`sha256:66b3089b1931f988214ee6a442f7966b661fe07ff5b2dda5f1f0322ad319476b`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 3.0 MB (2959100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f3bdc61eacb960d94ef556e398f699fccf564733bd2da28823c76f8f7c0a35`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:a48b5154172f728c6f004d19fce5595279e2b458bfc0201ca0e3816e6778bcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62445757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20fe8a14824c79c0c9bffb29c8ddd3c407e67eb07333b499b32221fb4d96b82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821308ee4c9feb5ee68751d20114fb10ce92c16beaed0ace13a46be48581734d`  
		Last Modified: Tue, 03 Dec 2024 02:39:51 GMT  
		Size: 36.7 MB (36686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dfbe4b0bce1279814a5df14570e61ad208c599cbbd41182ecbdb9c6ae92eae`  
		Last Modified: Tue, 26 Nov 2024 21:12:38 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6485d61cd96d997f217caace540592ad0f59e552bae1b795345a2f733936d3`  
		Last Modified: Tue, 03 Dec 2024 02:39:49 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1feffa31ad38feb0c4dec773b375f6d4b7c3f73a137d10d1022af07cd7f5af0`  
		Last Modified: Tue, 03 Dec 2024 02:39:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f31654bb758dda2e7f85ce21bafb064f01ca17d7d4b12df3b2bab4143e57bb`  
		Last Modified: Tue, 03 Dec 2024 02:39:49 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ece290b560fb0b271a8a071f279a8b81fa3a469a78abebc23e7a05f13a374e`  
		Last Modified: Tue, 03 Dec 2024 02:39:50 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:58d8e3efd07212bcfc8de56e898ccbeb08a5d5ee1d1a88842f6c9354059bb66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ef83cc7f27b97526893d6d7b65792addd30adeec48982c91bcebfd5c6efac4`

```dockerfile
```

-	Layers:
	-	`sha256:6bfdccaf52029e4ad35e3851991c98061db1c7adfa0e38684c6f371583723807`  
		Last Modified: Tue, 03 Dec 2024 02:39:50 GMT  
		Size: 3.0 MB (2980260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bcdcaa3f5fb1fc34ecc8a2b9d76c3b4df74e3cb05f26beb6e5c6dc0becd482e`  
		Last Modified: Tue, 03 Dec 2024 02:39:49 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:9f9c3c224a86552bfb9b59bc70d0beecb30e7d36b10f47c54108a0f9a6483c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60668989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeee7f08756fe64cfb888725b8bec52bf2f329d824b63c7980a6ddc33a9b5cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e271efbff756cd2b3ad42710b530a01fab73ec7f2f83e42a9920708cebcae73e`  
		Last Modified: Tue, 03 Dec 2024 02:37:34 GMT  
		Size: 36.7 MB (36730797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a5372c1f9a4b8fe137050a15278f1c83da2483127ba0a774eae73001566e79`  
		Last Modified: Tue, 03 Dec 2024 02:37:33 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dd5c68793c870800a94b033b5fbed135fe91c7dab0357abc3337cf472ca3aa`  
		Last Modified: Tue, 03 Dec 2024 02:37:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887c99f42eb15d266d6612b9a1efa32d268d38be5b59d27aa1cbad09ab8e2ad4`  
		Last Modified: Tue, 03 Dec 2024 02:37:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e53db4badbd0d4793ec78e03c8adac1bcf15f67c8a1bbf9c44733c52feeb1c3`  
		Last Modified: Tue, 03 Dec 2024 02:37:34 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3632b0bd36eedd34494d25ac51ad2327752b3278f63b58e42c820b9db0fe07`  
		Last Modified: Tue, 03 Dec 2024 02:37:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:cc62a2a4c048ffd8731554fe53d2f792de8ddc9deaac4eaa58fe5e36f97dd949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f2ddc26aa4b9527f492ab1bafc202e71c22a5121158ebffc718578999ee7b9`

```dockerfile
```

-	Layers:
	-	`sha256:2dd1cdcf106d67ee832214777b8779fef75ce50c3b36447b43cb0a8185e56d9f`  
		Last Modified: Tue, 03 Dec 2024 02:37:33 GMT  
		Size: 3.0 MB (2979227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e87c2373b7d9082ced1b13ba4d1d565a0dc10a8f6600019737aa3108729fdd`  
		Last Modified: Tue, 03 Dec 2024 02:37:33 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:6d3e464bc399ce5b0cd6a165162deb5926803c1c0ae8a1983ba0a1982b97a7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68503574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf62fd3a32f1209270ede068b6e08450dfe125c79b1a8ba8f5685090023bf7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bc5c1a6721e27a131b82427aa57e9723b9ee340dfbf0fa7ec5ff84973bd2a9`  
		Last Modified: Tue, 03 Dec 2024 02:56:55 GMT  
		Size: 40.4 MB (40440166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93f7200eab8466941579078401ed1bbafe71c233c0890b239f57c7baef7fa0f`  
		Last Modified: Tue, 03 Dec 2024 02:56:54 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd52ec2c0cb64cb574378a99d1340184ebe2b9c75278488ebe84951672943da`  
		Last Modified: Tue, 03 Dec 2024 02:56:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411a98463f95ef9f46fcdc448d9097338adf1e67041fb0b8517dc56fc5e56a00`  
		Last Modified: Tue, 03 Dec 2024 02:56:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5932596f7870c6c6fad6324aafdf8b56c335bff2f84525b9ad4b5e9fb322f8`  
		Last Modified: Tue, 03 Dec 2024 02:56:55 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25b2e5edb337e3cc06870c6b5e1a9381aa02b7a4de7e3f8925560565f6468b`  
		Last Modified: Tue, 03 Dec 2024 02:56:55 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:2f5550a872895ee1c62a7ecd44d0f85ba5e32ce01c2ae6b0ba3a7faa0de0e426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2994344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd38adc1db9f1b8fb7f15b849283f0652ba4fae2c35175c68769d85259edf7bf`

```dockerfile
```

-	Layers:
	-	`sha256:9a7cd349497efd3842969e64ae64043744a5958f25beb50fb0332d5f256f2657`  
		Last Modified: Tue, 03 Dec 2024 02:56:54 GMT  
		Size: 3.0 MB (2959550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20943f7976c4d0408d6c055822b27b090b50d910a4797e15edb78a4f40141ff0`  
		Last Modified: Tue, 03 Dec 2024 02:56:54 GMT  
		Size: 34.8 KB (34794 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:1c93c0fdf35c65d1a441ea049552faea6395ce4d5ad96258344d6e65d4c8c29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70416165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ba102d7db93bb0d93da1322102e3ab5c2486a9ea34245bf41508a0227699c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df43df7a475d2bf974fc9c24060cc1a694dae64cb6af0781fe5b15a08571e2a`  
		Last Modified: Tue, 03 Dec 2024 02:21:31 GMT  
		Size: 41.2 MB (41206071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f4bced9a55218f2c59ce24e9bbee7282f71a2ad45f25424081cb631a34435`  
		Last Modified: Tue, 03 Dec 2024 02:21:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2f6ba9fadce41e7bf1ae3a432cc0a49f0a13f79c28652ff870361246c7625a`  
		Last Modified: Tue, 03 Dec 2024 02:21:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d3e0deba8a7c4aaed9d1a3e4069acaabb007f7d9a5172ce8986d5c67e3b802`  
		Last Modified: Tue, 03 Dec 2024 02:21:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f00b64139edf5a25bcad7e9dbfcef836d54f183d8959d7f97c4bff3c5798a`  
		Last Modified: Tue, 03 Dec 2024 02:21:29 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b4e2f5a9b780a06ed7113b937eb4671bdbf0875e6a87926e02a37132531bf3`  
		Last Modified: Tue, 03 Dec 2024 02:21:29 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:cb0b90bfff0eb5b2297d3c2c9b3083474902422ec4b8efb022edc56c04a78315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3256b9214b0bda2b9ceb550c72440a13a178bdd17d3c03282b3949acfb2a5d`

```dockerfile
```

-	Layers:
	-	`sha256:5c7d42a88fc883a99fd4e23d91e55e612f7d38228d9ff9b8951e893ed2b875e7`  
		Last Modified: Tue, 03 Dec 2024 02:21:28 GMT  
		Size: 3.0 MB (2972380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21f0d30d5536502d7280a2a603810c0bf5a4aa892adaa4b3bc81e2eaa7a0b2d`  
		Last Modified: Tue, 03 Dec 2024 02:21:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:2af1ea73691294c5984f168764ec20267c61c91fb04d0c3036b3c8f487a4138d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68160700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122442871e8718a85b67478e8f9cc654d702a5d26793aeda27560c44c92a2074`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91009105a9e540dbf32da18bf030bdb43461beaf4c9b2930d3581f17e5b3c5b`  
		Last Modified: Tue, 03 Dec 2024 03:43:16 GMT  
		Size: 39.7 MB (39650178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666eb7f1b3fefdd4d076c6023246e151f56c1f1650900981fa2de2bbec5bcbe`  
		Last Modified: Tue, 26 Nov 2024 21:31:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f6abadab71b58e182a44eb121fc46e84999264025fbc834044255fbe75848`  
		Last Modified: Tue, 03 Dec 2024 03:43:12 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e24af7dce9d858f6c2c012eff5dab289d5df53d9fa36a9b9abb913130442b4`  
		Last Modified: Tue, 03 Dec 2024 03:43:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a5446f45d8ddf1b57230bffc63d30b0d71e5eb9ca3129cd2e3e46f56e578b`  
		Last Modified: Tue, 03 Dec 2024 03:43:12 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2ac71098b551d7fc808d3452920c3842b0a8229054187010a48952527160e6`  
		Last Modified: Tue, 03 Dec 2024 03:43:13 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:d004f1785c22cf3e8dc5daa8ec0b6a5704360235ad25044f4a42f2ef0578b81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd07977cce3af300dcfc0c63804f0f06a8ac21454bbe83c842eee3e94226d44e`

```dockerfile
```

-	Layers:
	-	`sha256:98f86d45723bc62ded6ba619053cc3651cfa983dfa95f980dc8989455a06b928`  
		Last Modified: Tue, 03 Dec 2024 03:43:12 GMT  
		Size: 34.5 KB (34523 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:190ed6acc1594ca343264368f3b369b0e19c05786ce27f80e71ee90d1feca38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76741393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd78bfdfa0a47da022a588fa4afce2ad0eb9ff2389dff2f4acca3d65debcfbe8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36cb70dac3e5b6e8427d4f86b3b2eec71790b517c3abcf4d230ea1b7bc9f9d3`  
		Last Modified: Tue, 03 Dec 2024 02:49:47 GMT  
		Size: 44.7 MB (44673529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96ea8beaf544c114ac20b36c7c39ed692eb591d8acd120c4d7ede58b7f861e1`  
		Last Modified: Tue, 03 Dec 2024 02:49:45 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab974fd4a918c76f4cd35bcad5b8d89a35e47972934681054201a51a4b97f9d2`  
		Last Modified: Tue, 03 Dec 2024 02:49:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2a2bbfefb6c914d9f62c12ad3c7033d7d57ba01b73666aa7c22abcd995c6d`  
		Last Modified: Tue, 03 Dec 2024 02:49:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadd74d89210f41518629b9e64027f84fc54579b5e14a49fb154b300357a5cf6`  
		Last Modified: Tue, 03 Dec 2024 02:49:46 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5dee3fc96f3c0eb377d9c037124be1ffbbe802a4893817dbe80286e986c8df`  
		Last Modified: Tue, 03 Dec 2024 02:49:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:785454908604d53fb68ba92e0f9d4bdd05a65aff1c5d18533f04a068887cbcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0915a9721190dbf6a2d8bb7a0ef339f606b3555a9ef8ad5befe80d9c16abb039`

```dockerfile
```

-	Layers:
	-	`sha256:0cfdaa54c91467c030e6d5a293b87b1f6ec447f2ec11a465b5c977da521db0c3`  
		Last Modified: Tue, 03 Dec 2024 02:49:46 GMT  
		Size: 3.0 MB (2986865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d2af876cbc4e52b8f06809f0630e46368cb9fafa13c33bf0a01c2abfbfe668`  
		Last Modified: Tue, 03 Dec 2024 02:49:45 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:7255c2465a7927453e4a5b92c927ae22659e47ec49226fe9774b53ea8cb02834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66767178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0c2cc6f664bc2cee8017a0833560eedd09795c2eee664636767ccf16b42872`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_VERSION=0.8.7
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NJS_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfc54e55de681421c485c6e7b00b9cadf8785c78c283d1d672a0602f2506a7`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 39.9 MB (39883611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d5dfa787410fcaf386c92623162c57cab6ecb9a97cccb3c02642fced1a25d9`  
		Last Modified: Tue, 03 Dec 2024 02:37:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3649a2e19818ac209ed4227f3634489875d72f7ed2411a8ee15049bddd0451`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438c69637e8be40b0aa642fbc6e68922cab12005e2eccfa13d2817f96197fea`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a586aba5145b09c40a5a52a582e825363a2b4027154e533564dd9c1755eba56`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef2ca942562d1ddcb5d5f95b131d86f4d76271f9c298bbc4447291e326b9c4`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:9a688530c9457e4205bedf2a6d39e4fa5a3f3d56b522819f51261607ae2d0419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3005068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d4697537808688b020cf7f18af1b9bc7292c41f8a472580404008834b6e05`

```dockerfile
```

-	Layers:
	-	`sha256:d290c152a5067d4ec03bdb9c887110e7bebf8710402195601394879710feeb03`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 3.0 MB (2970449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a24c41e59c7f2a17e8222e07d204be95dc806618410d9c1862082bc56ef8c1b`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json
