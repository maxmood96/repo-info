## `nginx:mainline-alpine-perl`

```console
$ docker pull nginx@sha256:3a59cf5243bc127a869861c945ff6cd85334975e70b5f109a51ae9e2618ba640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `nginx:mainline-alpine-perl` - linux; amd64

```console
$ docker pull nginx@sha256:1be4efdcae3f4675d7d2b2afeacae9c0cecb8b9fb07f5fccc37baf66787ca7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32399288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d9836b46c00c2bd9883280f0fbd294884513a4cdb0db9025dcb6606a108cb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80aba050eadb732c9571d549167ce0f71adce202ac619ae8786fe6c9eec3374`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 1.8 MB (1806628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a51978ed7f4a65a4324aaf124c21292fd986ed107e731f860572233073798`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e63548f2091b6073fb9744492242182874f6b2d2554c9f3a94455203a033f0`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce83cd996042dd16a6124be94e6046da71a9c6b59a6cc48704f6cffca76d7d`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d0ea5d3690e523d1c4fc7f288e0b98b6c405d5880fa11d1637483fd5afc74c`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb80c2f28bc872ae84429312ddfbc823aca17b7ce107a0f24074294cd3beac5`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c9bcaa4163e6fb844375a66c86911591b942e01511e28eec442e187f667f4e`  
		Last Modified: Wed, 08 Oct 2025 23:34:05 GMT  
		Size: 17.0 MB (16959526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5227fe999136954dbcc39028ca31cf5403a0ee370a8180ddf9405b39c9af5c`  
		Last Modified: Thu, 09 Oct 2025 00:13:28 GMT  
		Size: 9.8 MB (9826092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:895fa642ad4db11d8ff234970aeae4fb39f475f8db978b34e274950367cb7294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1831239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9391113b6238cb9a9382037bc49456613694caf0511ab3a34e0397202e10e963`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1a0570b6641ecac83351c02d66c6533e44114fec0740eb468c92eee392a81`  
		Last Modified: Thu, 09 Oct 2025 02:50:41 GMT  
		Size: 1.8 MB (1810274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efac8fe01a7050c974bbd8a08d94d23f601fad8bc9824555f0402eba05728ab4`  
		Last Modified: Thu, 09 Oct 2025 02:50:42 GMT  
		Size: 21.0 KB (20965 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; arm variant v6

```console
$ docker pull nginx@sha256:c81b09e61f5974d3468af6176f9f78cf7ba589d64b8babd322b90ecb14ede626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28378677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e096f1a1b7fe73208c5c3aee390f57dbc1c00b621738ad85b3bdac8b62e05e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc446d527adecc988050c2568d5bc9a7911d70dcbe5d95e8c21458763e7a067`  
		Last Modified: Wed, 08 Oct 2025 21:43:10 GMT  
		Size: 1.8 MB (1802907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55449b67b0c4922fe1a696364be990a912379fbfde94013764283bf49056c548`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc87a95d2bfffb45ccdcbcd2b5d90848fc58c478456b55d1a31c01f09abb964`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a65cf31df5ec725614470c00cb14a081e1b912963acdeac5c749b7bb8ced3f`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511722a3e1aca60a2d98ac08b87c774251716de3532346b5c0863140bad8d2f5`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f370778828565f33258329323b59504ea66778db48248b6403c81d85577eae3`  
		Last Modified: Wed, 08 Oct 2025 21:43:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50d17e70621d75729483bf61f96c46db5d300ca90bc47d4ca5af93bdc916da`  
		Last Modified: Wed, 08 Oct 2025 22:59:09 GMT  
		Size: 14.0 MB (14010763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd599a67296d3797cab6fe9840aec2909f03263475d46e0de19873e63336f1c3`  
		Last Modified: Thu, 09 Oct 2025 00:12:35 GMT  
		Size: 9.1 MB (9056328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:8c8af7f3e09338f8ab051a7647f319351430835d3aef0797bb983bafc87221c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688ea442d6f68c841cce4bd0b27354c5c71ebe98115a08f2b459f511fcbc37f`

```dockerfile
```

-	Layers:
	-	`sha256:52ec590d7622b9086ead840be45841c14ef45e2fe056b77775da7bd0cd7ccb70`  
		Last Modified: Thu, 09 Oct 2025 02:50:45 GMT  
		Size: 20.9 KB (20878 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:d95d22a29d583bdc7523669e676b93755fdb3d1ce5d9f2ae4292659cd59e4140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27991819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b920aa36a1a00bb5ec03f9b6efdc07337f854ec948f8b8526e243c4af1006cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0275b4735dec2e21942d9a4b5b976d8c8a8fe47e686100d264ce04aaed4ac219`  
		Last Modified: Wed, 08 Oct 2025 21:51:39 GMT  
		Size: 1.6 MB (1638330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b186f27279fa9f7e97169be5420185ce0650263514b86b286dcc3372f13ee9a`  
		Last Modified: Wed, 08 Oct 2025 21:51:46 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88c7b91095f9fc3ff8fac959f2e225eabbd7661c3b3dedf16735c6a50c4443`  
		Last Modified: Wed, 08 Oct 2025 21:51:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd8e8474bc2b67b2e6a57634ba471b3c5643ac8e2937d31ad4479e8e6d61bdc`  
		Last Modified: Wed, 08 Oct 2025 21:51:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9967daca834b54f525e146a4735c57c60875910e92215e6a8e2def4e9e0d8ee`  
		Last Modified: Wed, 08 Oct 2025 21:51:57 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effce4a12f878f88f222ff610de3964c757a8bc002b4fa8ed35ad47e927d3566`  
		Last Modified: Wed, 08 Oct 2025 21:52:06 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1febbe51bc88031773a76e38d20703a0dd8ebff96932100b63ff5d5e716d973b`  
		Last Modified: Wed, 08 Oct 2025 23:17:08 GMT  
		Size: 14.2 MB (14241021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324aa550f75b653edc8e84fa020c8a0d8ef9266304a0d94d0bf4bf49a3b832cf`  
		Last Modified: Wed, 08 Oct 2025 23:44:03 GMT  
		Size: 8.9 MB (8886315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:d2d832d6998d29ea6ab142a3ad9410756d3d63e629879e28a87a542133fc936b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1831463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8ba4fce2345e94b3a94dbfdc711c1b833ff46fe586d050072c9d96148c6aa0`

```dockerfile
```

-	Layers:
	-	`sha256:78c8eba8b938984c20f6bffc7b0ca7ad1027a9285072ad3a4e34e23bf6d04ac1`  
		Last Modified: Thu, 09 Oct 2025 02:50:48 GMT  
		Size: 1.8 MB (1810370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220bfebe06a941e0b4a3066550644dbc7e199bb79669bf11df39dca03106c60e`  
		Last Modified: Thu, 09 Oct 2025 02:50:49 GMT  
		Size: 21.1 KB (21093 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f9fbca9dc83e9ea6b17a4ee09f058327dd3938ea127c6305114072bdb66519a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32844357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b394204205eebeabf5ed73f89109363345c0b5ad8463df9fad04207fecae9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f96c998a19d54b6743aad088bd952f544117f90a4ccdac96a4242cddb0633c`  
		Last Modified: Wed, 08 Oct 2025 21:29:05 GMT  
		Size: 1.8 MB (1801404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e2acadaedad6abad1f0fdff3769f509d728669e216cba9e1c9e6fc7621aaf`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9053389e18faf515b463ba1394792c0668d07a61effb4807ba02ca95f9a4f89f`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79803634f1ebc24b6f5cacc6a2596bf83fc2ff3559d5db94e8d22be4e04cb4cb`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaee67c1f064f409e4dd10237c010db5125183de4bf1937e39ee1c549cd6609`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f03cc2091c9c59915d01173c8f7c51f3dc20f4ae04d68f34229e6ffc1165046`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3bb55b328c560d1583744d6b6848357f3ae586c319287fc60ac7690692b214`  
		Last Modified: Wed, 08 Oct 2025 22:52:04 GMT  
		Size: 17.1 MB (17110961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb9627615b45e704160d665c6221a8adc35c0251f0a93ca7330bae185d7bb19`  
		Last Modified: Wed, 08 Oct 2025 23:22:30 GMT  
		Size: 9.8 MB (9789334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:f9df99ad2fa3180f7e266f0a3f9d8d2c109eeaecc32b751d4560a3f7bd9004ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1831545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c238be715f4801aa3b4513c2bfc1312b29e933d19a5c99a1e5a7a2b526748299`

```dockerfile
```

-	Layers:
	-	`sha256:efb3fd5d818610d747b0871f778391e46e9e024136e091743c7771e699ba16e9`  
		Last Modified: Wed, 08 Oct 2025 23:50:55 GMT  
		Size: 1.8 MB (1810404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7b35560555569f0825647cb05dbda914152374513ca463c62695d367a96003`  
		Last Modified: Wed, 08 Oct 2025 23:50:56 GMT  
		Size: 21.1 KB (21141 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; 386

```console
$ docker pull nginx@sha256:b3b16bb8ec9ab4cb8c7c9b89579cce46fed4f4d32f761cd0fce63b61f86f2386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31115087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1671b290a5132e602aa4fc94a913cceeb3af729396dc4212599b5d0e5dfc58bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8310ca5f31389ac16c335f0c59554ff102f0cd5506cb036a7bf1cb1adb140ba9`  
		Last Modified: Wed, 08 Oct 2025 21:14:25 GMT  
		Size: 1.9 MB (1875494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cfd06ba18372210f0049c0949b4f3fad822b58e36063ee8ca5b85f48b43b79`  
		Last Modified: Wed, 08 Oct 2025 21:14:24 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c217ef5ab5559cbb5ef654f5f9d930e4cc0e2bb036ab81ae25edd50c80b94e`  
		Last Modified: Wed, 08 Oct 2025 21:14:24 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3556f4cfae77206797e5b9a6fe4d591102a2ba2ce18562b912e626c98e6b2`  
		Last Modified: Wed, 08 Oct 2025 21:14:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f34bfda3c2cc938d0f7ddeb34ffb67b84ecce479ffb3c9701c62f7efda5dd`  
		Last Modified: Wed, 08 Oct 2025 21:14:24 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7313e5b2f789ebf3bd27e78ff79242d79acfb98d63d3b1f1a0987ecb39e5eaa5`  
		Last Modified: Wed, 08 Oct 2025 21:14:24 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d945d6546ffc8e6f28d8095601dd60d684152ed0ec3f6abaf6d8efabe3a106`  
		Last Modified: Wed, 08 Oct 2025 21:49:16 GMT  
		Size: 16.2 MB (16247063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d949f1c95489d9a3591d351a2bd6ce8e633ecad719ddc9eca55d6149085c9f`  
		Last Modified: Wed, 08 Oct 2025 22:18:11 GMT  
		Size: 9.4 MB (9369002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:277bbc66562a494dca841c8988f8e874706ef454f953bd65bdf52f00003ff44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1831130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bb41928994766b58b45e9b5cdd167ade86a48ac014c74c7c033f663404136`

```dockerfile
```

-	Layers:
	-	`sha256:8e481223507090f53ddea624ed7652e52e8f25912b26f224d2fd2468ee1f4135`  
		Last Modified: Wed, 08 Oct 2025 23:51:01 GMT  
		Size: 1.8 MB (1810227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9aa74902525994d8caac3daaa26560e17f2adc175b5ea2ebda64d014dacbb13`  
		Last Modified: Wed, 08 Oct 2025 23:51:02 GMT  
		Size: 20.9 KB (20903 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:d0b0677c675b6cd90dd0279b0620f8ee5b966741e9b743525cefcb5fd445d528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32899975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6088ae1a4c199dc4e7f4cf1d529a535d03bb75991251c0e6e8170a5bd4d1062a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3260afb518ba06dd5aa3b278046d1a99bdf81dab768a44be5ab6ab962a5dfc8`  
		Last Modified: Thu, 09 Oct 2025 00:50:22 GMT  
		Size: 1.9 MB (1867408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b014981c91cf19aa78d00014fb730677df86df47dfca991e235bf91f0196acf`  
		Last Modified: Wed, 08 Oct 2025 00:22:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe555495d70cf18ec081178c7a82efc7700cb41b526d9978d1b7a7c75da13ce`  
		Last Modified: Thu, 09 Oct 2025 00:50:21 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd985118ce017517b14803c6f459e256cdf8d60940519c3b0d4e1318051491b`  
		Last Modified: Thu, 09 Oct 2025 00:50:21 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566578ff744e79a64b60d2c5b8e470471f7c4edb9fe4f5078ebcbafa1f88c50b`  
		Last Modified: Thu, 09 Oct 2025 00:50:21 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d837634586838aad6068cde4c1c03acb9cf95523320bb18768308dba620ce59d`  
		Last Modified: Thu, 09 Oct 2025 00:50:21 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1527c41e6b2034f4fc05fc14bd9a54d5758ec4d5d4342b9dca11457f1173fcd`  
		Last Modified: Thu, 09 Oct 2025 05:24:09 GMT  
		Size: 17.3 MB (17278125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1476943aca9a26110ac97e42e9f7bd5d0fe6f03f15ab3f266fab8b316e6c6bc`  
		Last Modified: Thu, 09 Oct 2025 11:12:34 GMT  
		Size: 10.0 MB (10017595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:994f0160a7138ce4b3c25cc796cbaa49a337ab265f140b53eb71158eb5ed926b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1829441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12d85c2fb94139a1548f51f53db5a6531c243df893cc01a512716a54b3b4e4e`

```dockerfile
```

-	Layers:
	-	`sha256:2f6a343ddbc4c72834abd47558112c554c8af6c6718df2053c12d5df2407a7b9`  
		Last Modified: Thu, 09 Oct 2025 11:50:33 GMT  
		Size: 1.8 MB (1808395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72859f46796a465eee9b5abbadbed56bce6f97f4e1c9e682a4c9262b840026`  
		Last Modified: Thu, 09 Oct 2025 11:50:34 GMT  
		Size: 21.0 KB (21046 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; riscv64

```console
$ docker pull nginx@sha256:ac71034571ba2e031b8fde1f13d98d258b3957005a4dd3066aa00edc782dd24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31795220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c201c9e6c974ad3ec811a856da48ccba401d5fc59d3fad23c18076f12aeb706`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 18:59:57 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b87a23a19ad5395bbec2fc608f5afbc64de997d77aa34fb03ee4cc37ac3437`  
		Last Modified: Wed, 08 Oct 2025 09:48:10 GMT  
		Size: 4.0 MB (3980856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e74138c4c7f9d86fc3e173abf8889c0b7f070083c67c7b832807fa29ab9414`  
		Last Modified: Wed, 08 Oct 2025 09:48:09 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e30774bb50963905a0be06ea859ebd597f5b51d44d9c89c8935d909eb8ebea`  
		Last Modified: Wed, 08 Oct 2025 09:48:09 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71965a5ebcc745bbcca60d850f4f73efadaf3cdf54f62fc3fc86b996055460a3`  
		Last Modified: Wed, 08 Oct 2025 09:48:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bd0fce9402afd079eda9db51ce56e288156363630b97f0f80f5b9a6f475a7c`  
		Last Modified: Wed, 08 Oct 2025 09:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faec6ed300f4753f48a5f31ed218e7429f65e8376c9dcc4b5370bad61ab281d4`  
		Last Modified: Wed, 08 Oct 2025 09:48:09 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ecc18e848bf56a90ca2fb3bcac0572dca7572b4460e95d649c13cfc648d855`  
		Last Modified: Wed, 08 Oct 2025 12:26:15 GMT  
		Size: 15.0 MB (15024395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a9634a52c2f9c77a66d9bdca103a13ee78af720cf1b8b071c7c28dc492609f`  
		Last Modified: Wed, 08 Oct 2025 13:14:30 GMT  
		Size: 9.3 MB (9272565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:895dba8a5802624c9352069fd9dcb0aedb7aeeae5440fb5bcd29944decb869fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1830519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a111ef4626d53cf5200c78415f54c505e3f3a4005124dc11376399475e075`

```dockerfile
```

-	Layers:
	-	`sha256:297286d71c293ec433e89fd46ad91415b42a8718fb8529f3fe557113c398f5d0`  
		Last Modified: Wed, 08 Oct 2025 14:50:42 GMT  
		Size: 1.8 MB (1809474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d9bcc0f7c409baf22af8557ff0304d00e397b561ffa595b8187e03cc48214f`  
		Last Modified: Wed, 08 Oct 2025 14:50:43 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-perl` - linux; s390x

```console
$ docker pull nginx@sha256:f2a7d0f7db470d6e37629787e4e7804d4f3687b26dd861770f4e9a1ae3da8866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33195410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a4aba5d1d14d4436e8f64580f212a42ce5487d77b270ae8186866a34859b95`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 07 Oct 2025 21:06:46 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NGINX_VERSION=1.29.2
# Tue, 07 Oct 2025 21:06:46 GMT
ENV PKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
ENV DYNPKG_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Oct 2025 21:06:46 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Oct 2025 21:06:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Oct 2025 21:06:46 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_VERSION=0.9.3
# Tue, 07 Oct 2025 21:06:46 GMT
ENV NJS_RELEASE=1
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b6023cfc9c40d2d1803f7a03229c10bb6c63738eba2199f13a9a15bacaeb6`  
		Last Modified: Thu, 09 Oct 2025 00:50:05 GMT  
		Size: 1.9 MB (1908435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca19445ad502608aec295f55683f5cd1ddeda8521077f3493fa4b1b02d0184e`  
		Last Modified: Wed, 08 Oct 2025 00:25:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b408c13a0ef3a447c0e73228d1823b5eaaeb597a59372557f7e00a2422ea9b4`  
		Last Modified: Thu, 09 Oct 2025 00:50:05 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647ea3a7c05e2ef2380ee75e7e3bff603ed3713a661e4078fc81a0807ee70db7`  
		Last Modified: Thu, 09 Oct 2025 00:50:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab760fa73aebd42c06e8b6ca053a55983b13d006309e2071f7f30a8204e743d`  
		Last Modified: Thu, 09 Oct 2025 00:50:05 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22832d2bb661c9f3bcf50afde96f438bdec54fad66654053fa576f44b0a72a5`  
		Last Modified: Thu, 09 Oct 2025 00:50:05 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e560ade9a499d5068f6a95a468b3c3254587a5e783f10fd43164191701b0b76`  
		Last Modified: Thu, 09 Oct 2025 06:23:10 GMT  
		Size: 17.3 MB (17257343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f90d80efdc1cd09f0b1d1ab2d195161dd1e2adf5cdf7d369f397aaf259eada`  
		Last Modified: Thu, 09 Oct 2025 14:32:14 GMT  
		Size: 10.4 MB (10375780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:92117134201b66d15a77d7da75b1ca1890aa4083f4430aab603af1cb035295ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1829287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c6d76df8abe611a4f4af9c3cbb9802b03e24f6e530769edec9080880afa562`

```dockerfile
```

-	Layers:
	-	`sha256:9ed091f316d60732e0af10616e7989d1522f088883b3230773dea6173ca30a88`  
		Last Modified: Thu, 09 Oct 2025 17:50:41 GMT  
		Size: 1.8 MB (1808321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e1bb13df096c4888bbe6f5d4b520b333b5fbfee7a5f87111ec1052ddc89882`  
		Last Modified: Thu, 09 Oct 2025 17:50:42 GMT  
		Size: 21.0 KB (20966 bytes)  
		MIME: application/vnd.in-toto+json
