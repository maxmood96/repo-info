## `nginx:latest`

```console
$ docker pull nginx@sha256:0a399eb16751829e1af26fea27b20c3ec28d7ab1fb72182879dcae1cca21206a
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

### `nginx:latest` - linux; amd64

```console
$ docker pull nginx@sha256:2426c815287ed75a3a33dd28512eba4f0f783946844209ccf3fa8990817a4eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72059409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bea9f2796e236cb18c2b3ad561ff29f655d1001f9ec7247a0bc5e08d25652a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207b812743af01771d6c94b3ebc59543bf3c6fefe5d4d9ebfa6e5e5558801d34`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 43.8 MB (43842390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e383b441eda86c164d8e833da080b951c951d612853cac2fd44eed0d72226`  
		Last Modified: Tue, 14 Jan 2025 20:32:57 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0256c04a8d84ab5ae434b607055df8fdfe0278dba43f3e603a861dc7e26da395`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e992d287c563d332ed8c9bdefec32a84f50f94cc39bb4729a3e73cefde88eb`  
		Last Modified: Tue, 14 Jan 2025 02:21:15 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9aab598f58e86706b73c23e0ff33fc4eb60a5e69424147f9cb7c02e853323b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de87b37f4ad0b499be3db4cc6831db3d8158867f12dabc0bf42046b56784d3b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:31098f833ac1eef55e0c9d892b4dde9a729de85679799b63dcb407a0c9c3db9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935dfd3606d35a50beefb99c32122ceec920cda29ed946dd363a52dbbab736cc`

```dockerfile
```

-	Layers:
	-	`sha256:77dc589177a5e755e0f7ee5cb296725ab195bb882f04f7fc071f3dd2b1c21292`  
		Last Modified: Tue, 14 Jan 2025 02:21:15 GMT  
		Size: 3.0 MB (2956042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c03a32d599e93c0c697423086c9975f879c3695a394e7b66dd52608a3359103`  
		Last Modified: Tue, 14 Jan 2025 21:00:58 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v5

```console
$ docker pull nginx@sha256:0c69075a39f218db0dcdb3262d752abe132e6b7979a0773ce7e1a6d91ec6580a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62427789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9773a590682c62f3cb3527d6bf0c60dead3976e0673a02aa1473308afea6d7aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbbca9c9d1f8488b71159e6b2d84be150ff0cd689a2cfa38674b9cd323de587`  
		Last Modified: Tue, 14 Jan 2025 02:40:11 GMT  
		Size: 36.7 MB (36686521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9bf0c5da27d1f741ca9062576059c10fa62b62af2b71e6855335d7524c21b`  
		Last Modified: Tue, 14 Jan 2025 21:06:10 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bae8d9f06e249c80fb70504d29a7253f6fb76c8e7cd48a81f5cf573c9eb997`  
		Last Modified: Tue, 14 Jan 2025 02:40:09 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f902e0495f318a3ed5fac2b3c25341924d819edf22acf1cf3256c385e3652cf3`  
		Last Modified: Tue, 14 Jan 2025 02:40:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2be25cb07d4bd78ba00f71513612657f359f0a2336830270c51c627205d31bb`  
		Last Modified: Tue, 14 Jan 2025 02:40:10 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ff9a845d1a44cab249d59156c0c373b048920180524ab78cc1d714776515c0`  
		Last Modified: Tue, 14 Jan 2025 02:40:10 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:ab8f7c53d916f59b071c030e1e230294492bd4e9e116af43a2d3f5ae20313180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fa38d71b0deac71c452c9c1788f29442b18652222335ddf72fc83a9a8e68b1`

```dockerfile
```

-	Layers:
	-	`sha256:b2c6e00b6d1ee022453ceff91e21c0e1127587f9684305a9b2087141ca4da207`  
		Last Modified: Tue, 14 Jan 2025 02:40:09 GMT  
		Size: 3.0 MB (2977265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bec5658938e3bb5dacac7b2cd06860e7ea2cf082bc794f87f142d2fe8841962`  
		Last Modified: Tue, 14 Jan 2025 21:16:03 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v7

```console
$ docker pull nginx@sha256:12c70a7ea5cb416f7dffbbed7bf06d3aa0c62b920c5dee6bea911d44b8d30458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60650734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d61aa644fde32d98a73d7bef2340f3d4941463a0a50f383668e2c4bc559985`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea9b9de154dcd1e2df52b50a4a42abf49edbb060e6b37d0eaa379350e9b7620`  
		Last Modified: Tue, 14 Jan 2025 20:35:43 GMT  
		Size: 36.7 MB (36731531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febb66ba235a663d5422785e0c2041642e7eb2f10b38bb42fb2ab8bf4b3b3e`  
		Last Modified: Tue, 14 Jan 2025 20:37:51 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2e3f1fa5f3be5b2193cb68699d548d2fa1603753eb1ddf29744834eeff7bdb`  
		Last Modified: Tue, 14 Jan 2025 02:40:28 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbf0c76f4dc2e8873a4e6bcb95adf5cac219815fc1749a375b1dde380d6822`  
		Last Modified: Tue, 14 Jan 2025 20:35:40 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c271f9bc3cbfcc2c941a2cd8f614b725cd188067d77780990e7c237bf26a3a20`  
		Last Modified: Tue, 14 Jan 2025 20:47:52 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3447122d076b67312328862ad201520464ebdb1cf1c3c61c98c33e25e7dc04`  
		Last Modified: Tue, 14 Jan 2025 20:35:40 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:0560878623ce09c41162c81e5744033efca1f07a865c3c42dd3520167b368059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96d4542add98d7e56f4e8f20fa4b49adbb9a0ed579ab7b080cbbca481a8bbfb`

```dockerfile
```

-	Layers:
	-	`sha256:b73ae75dded948e2000d8350e4d736456799d8fd0d8c6089110d32c83b5f5882`  
		Last Modified: Tue, 14 Jan 2025 21:01:02 GMT  
		Size: 3.0 MB (2976232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b139c230c43488b8e8794f5f8a369784b6d1b6b60667bd58b970d9d51d7c68`  
		Last Modified: Tue, 14 Jan 2025 02:40:28 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:5ad6d1fbf7a41cf81658450236559fd03a80f78e6a5ed21b08e373dec4948712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68485942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781d902f1e046dcb5aba879a2371b2b6494f97bad89f65a2c7308e78f8087670`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e9225c8fcac3ce978be9e04d8f3ea218a29e28323749716b11ace6671c49c9`  
		Last Modified: Tue, 14 Jan 2025 13:07:00 GMT  
		Size: 40.4 MB (40440316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39a3d0829ec9fa7c704381345b88825febd46b7807544b559ee14b3a291abf`  
		Last Modified: Tue, 14 Jan 2025 13:06:58 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24e34787c7f34bece65419c7ea6a34ac15e918659c30e1670d03b327436eba`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d623ff8e645b5b10e3bcc7a13baf9e4dc0a28f58549e47dd750bd7f9a6822`  
		Last Modified: Tue, 14 Jan 2025 13:06:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49486a4a61a65bea828604e0a7dff6f3583954e0fd17742437f654f43c4938ba`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d83bb3522a8af3bdfb0d04e6bc3c01ee02ed429bca8eb94380de8470fe97ee`  
		Last Modified: Tue, 14 Jan 2025 13:06:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:9f18eceede2d784f11af93e1bd63b06bc291619d1baedcbc5edb45db075a0529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6e865698ce5a03cf8943277fa64299375542dde1ab87d7b8af0d2fb2605c61`

```dockerfile
```

-	Layers:
	-	`sha256:04218cf0280cd1df3939bd8a294212086122d13767cb844c25bdf71ac5932ce8`  
		Last Modified: Tue, 14 Jan 2025 13:06:59 GMT  
		Size: 3.0 MB (2956493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a744b69a7663797366dee65bd3e8c5ff927ef19bbebd43a5c88e5c096b05cf3d`  
		Last Modified: Tue, 14 Jan 2025 13:06:58 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; 386

```console
$ docker pull nginx@sha256:b2607311d3192da3dc969583d18a7fca2af2a6189321549a3fabfc0f1c95364d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70398308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4009deb1d41d4d3faccd0d05b80894e3fd2fa377f433197a0379bed89e0602`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d4f1b415b12f1ff1f4096b54a30782af517ebb1dc6c27f2ad2d1b46d5664fd`  
		Last Modified: Tue, 14 Jan 2025 21:16:56 GMT  
		Size: 41.2 MB (41206111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3b376aa55f1da79c21b63861a1f8ee726af8083dd94a46808da1329059136`  
		Last Modified: Tue, 14 Jan 2025 02:21:16 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20e59cc2dc435ffd0affcda7b0a4e3fdc26a327d26d645a7dcc0ba6f7472a93`  
		Last Modified: Tue, 14 Jan 2025 21:06:13 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27257f63e15dde0c66d398ca3e6d1f745932db55719f29053d3f8113402f62e1`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5088b30a3afc0db02d9c62415a7e5055bf54de4807f274f4f84a633cb2f75298`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087cc35c393fe5af4f94c9e332a86ea4f8c039c555a81531e948f6204ca8668b`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:91aacc4cf1c6f95cfab0d27bdd84d0d1cfc77b986e093eb48d15e2f6d67fe435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3003870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d9a41560f73748b1cc278300c73d94b35d3d7f3255e13946355b85c799f88c`

```dockerfile
```

-	Layers:
	-	`sha256:e6f68f2530e883cfa7a0a763c1a584c1fca56fe0dff0fb7fc525a0dfc9b53834`  
		Last Modified: Tue, 14 Jan 2025 21:01:07 GMT  
		Size: 3.0 MB (2969313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b390f258325f62d4503b9228f3ba76e3e6417ea8bbc981c76269fb75387902`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 34.6 KB (34557 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; mips64le

```console
$ docker pull nginx@sha256:cdae646f61e00ebdaee4fcd51100f639ba820b6e9f388a1e3e139f515e5fe7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68142004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a81afd641fb8a600d127e31e5c33e899ad1eaa7ac1652feda10e1a2bf1e413`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ada6be39b3aa4500f8069eb78d6126c12df920ddc9a3633b47ded4a19485b`  
		Last Modified: Tue, 14 Jan 2025 21:06:18 GMT  
		Size: 39.7 MB (39650752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf03e2944f5b59512cc4dcdf71d2a9306b7cdeb89cff0d2bb722bcd4e82d203`  
		Last Modified: Tue, 14 Jan 2025 03:45:14 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4e1853996b283fbe911d0ae255fe7f52d55950dc0bd5f76323db64fdec006e`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481872160d95aa1cfab8666493894dc743279503108b7ed6f48fbf022e5529f4`  
		Last Modified: Tue, 14 Jan 2025 03:45:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23150b4fd846c9609f39ec62b3ea1376370d49befd71c92f101e017a614cb8ef`  
		Last Modified: Tue, 14 Jan 2025 21:06:15 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c9efb33db977b03fb8ca8503ad8b6253d1c06c9da41736057d6d82a2a5e67`  
		Last Modified: Tue, 14 Jan 2025 03:45:15 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:f486e8a31b4442ae186dd1fb72c39f7c8a67956e02ac1476a148c7a2d2f04da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b17bc155f96bd8ece61c85671b46129e3786feb8f4d5cc8d10974e3b43e533`

```dockerfile
```

-	Layers:
	-	`sha256:e21c9a604e4d41ad99675e0cd511966fa2a002debeccd0acb9529cf0de2490a9`  
		Last Modified: Tue, 14 Jan 2025 21:06:14 GMT  
		Size: 34.5 KB (34523 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; ppc64le

```console
$ docker pull nginx@sha256:40f3a2e9853373d3bf77e7a99fcfc1d212605ea8eea5c0c6d580c7cfd8cdf441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76723247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c26ca84855f8ded0821674ecc0cc38a0bdd6c280878b95dd597457857643066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3923c1c318ec3764403fda738a26ee44793818ee8fe2ec8b6c194d404d2067ed`  
		Last Modified: Tue, 14 Jan 2025 21:06:19 GMT  
		Size: 44.7 MB (44673797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85012713814d9161ba28729bc0b5f4f195c9d439b3911e6972342dff50ebf`  
		Last Modified: Tue, 14 Jan 2025 21:06:15 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7284c4ce0b38bbe85bbb01657da27a42a00bef6b6b520acc75d5d82d7685ad6`  
		Last Modified: Tue, 14 Jan 2025 03:09:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf547ee08cc28cba787ed07677182aa74f60ba6bd207062eced83ef480ff188`  
		Last Modified: Tue, 14 Jan 2025 03:09:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbbbe07cb53802a7edeeed2a1cd1620308dfee632aac1ceeca4cd000d1f4062`  
		Last Modified: Tue, 14 Jan 2025 03:09:36 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9ce9a970e1982ee1d46305cd9efff844f304f23bef08fd0ccbd72cf4ca1388`  
		Last Modified: Tue, 14 Jan 2025 03:09:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:7fc41a91a8f6505ada5fc6981427f90a5fee026c02eec06102d5130f42bb7e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3018522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33400de06d026f3b44b4832e229d6cd07dba6edf60135eadc30bd091505ccb0a`

```dockerfile
```

-	Layers:
	-	`sha256:3d9095b1a8aa0bf295a100686c3dc58ba6e5593cadcd8ecb80f09dd61c02d7ea`  
		Last Modified: Tue, 14 Jan 2025 21:01:10 GMT  
		Size: 3.0 MB (2983823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4704de92a437077f08fee3dc43d26b98a6a499ffb171a4d9c11a9a0f84a7cfcb`  
		Last Modified: Tue, 14 Jan 2025 21:01:11 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; s390x

```console
$ docker pull nginx@sha256:c9a74cab828ac9bdd2e235e823dc4736a4d15ea46c3d9dab41be7bf03a2ea7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66747097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346b6b2f81a97b4ef8bb7ee01bda3ba4355b233dd4ca1d579d7336a32ea659c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0dfa9b75508048f197015574fba55f51eeb0db1cdd1948af6977b724d7dea1`  
		Last Modified: Tue, 14 Jan 2025 21:06:21 GMT  
		Size: 39.9 MB (39883759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc903f289122478c08f30b2d05b8b0cc738d6df0b6add137c5accd48206fd85`  
		Last Modified: Tue, 14 Jan 2025 21:06:16 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f97e7553540281dbddf0d7262c523dc019972870de04490efca9ad8ba6d7408`  
		Last Modified: Tue, 14 Jan 2025 21:06:16 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133988bb3feded4691d2e1ff09c3e997e21d484336ae88aab42786ae8a1fafcc`  
		Last Modified: Tue, 14 Jan 2025 21:17:48 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae78f0c689880af0fc9f916333d934374fecac8e4b369eb4bb0e0f6cebbfa115`  
		Last Modified: Tue, 14 Jan 2025 21:06:17 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1214eb7e8b1e8e1439d060a372ae2de0ee83287a325da139ca2b83b6e35769`  
		Last Modified: Tue, 14 Jan 2025 21:06:17 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:3d2d08bd88f4e4a33d23ce57345dbaf81cb3fa712fd269a704f33e6dd3fcb119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3002054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26fc9fcf7d29ee92fbc04b6ab86b8f91bd47ffa5627cf3fc0362482628ea2f3`

```dockerfile
```

-	Layers:
	-	`sha256:1b632dc0f5baa81320cbdea9a2a2241812c82bcdf30020651114621a5e5d845e`  
		Last Modified: Tue, 14 Jan 2025 21:01:13 GMT  
		Size: 3.0 MB (2967435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdac76ccfcf38c39ecd29af4cebc7b01c7e3a4d4679d1bfd249a4fa7890be73`  
		Last Modified: Tue, 14 Jan 2025 21:01:13 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json
