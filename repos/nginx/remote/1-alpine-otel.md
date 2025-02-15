## `nginx:1-alpine-otel`

```console
$ docker pull nginx@sha256:3ad29d001ced82908dfec6ac29ad329b3309efeb1224b23370903b47fcabcbc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-alpine-otel` - linux; amd64

```console
$ docker pull nginx@sha256:4c84537930543d88e59a2255d542f43a1870257326ef453292a6849d10649404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34102049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa32c75d9d0933cead018054e8aad3e0c725e0980935537637947c87a007527`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.27.4
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_VERSION=0.8.9
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENV OTEL_VERSION=0.1.1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc35e35d420d6dd115290f1074afc6ad1c474b6f94897434e6befd33be781d2`  
		Last Modified: Fri, 14 Feb 2025 20:33:41 GMT  
		Size: 1.8 MB (1788871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2ec460bdf5babee56d7e13b060b308f42cbf2103f6665c349f0b98dac8962`  
		Last Modified: Fri, 14 Feb 2025 20:33:40 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984583bcf083fa6900b5e7834795a9a57a9b4dfe7448d5350474f5d309625ece`  
		Last Modified: Fri, 14 Feb 2025 20:33:40 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27c072a58f81ecf2425172ac0e5b25010ff2d014f89de35b90104e462568eb`  
		Last Modified: Fri, 14 Feb 2025 20:33:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3286a7346303a31b69a5189f63f1414cc1de44e397088dcd07edb322df1fe9`  
		Last Modified: Fri, 14 Feb 2025 20:33:41 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79cc6084d434876ce0f038c675d20532f28e476283a29e7e63bc0bf13a4ed6`  
		Last Modified: Fri, 14 Feb 2025 20:33:40 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e4c092ab716c95e1a8840943549b4ac5e6c5d1a1cc74496528e1b03e1e67a`  
		Last Modified: Fri, 14 Feb 2025 21:11:06 GMT  
		Size: 15.4 MB (15375003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0cf8e80f97b4a847f9e5e46af6cd5876652371d4586b9e915aad2210e3b40c`  
		Last Modified: Sat, 15 Feb 2025 01:00:09 GMT  
		Size: 13.3 MB (13291341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:452f2796defa77bf3cf025f38b2cfec8e5390dd32fa8c5aa2b24b317833a8845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1051030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a9cc9be34fe95ab0ea40e593979dc5a483bd0ef689d99f886710d3e559fae2`

```dockerfile
```

-	Layers:
	-	`sha256:d37b771f826c61ff095652b24c8084ee1866e6d6d94fc71a10289014d8c5cb81`  
		Last Modified: Sat, 15 Feb 2025 00:50:24 GMT  
		Size: 1.0 MB (1029672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6866e42f76d1e96d04eb5d9f7a51a3224f5eaa174d88786a21398de4c5dbb1be`  
		Last Modified: Sat, 15 Feb 2025 00:50:24 GMT  
		Size: 21.4 KB (21358 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:5ebc9be2d289ac55a1986521355f065f01cabd783341d87f432bd3ac613ec5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34433981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2687cb1fe1c4a242c82451bc8a57307d38119b0bf0ecb4d6a82476e7cbeada01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.27.4
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_VERSION=0.8.9
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENV OTEL_VERSION=0.1.1
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be31969a6d1e1f2699d0fb5a48f1b4da62a3b2aefa8a9b0dfb548bc497bf321`  
		Last Modified: Sat, 15 Feb 2025 00:52:37 GMT  
		Size: 1.8 MB (1780385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e170776f94c97f95260908e78676599218d0247c22929326f7072689b832bbb`  
		Last Modified: Fri, 14 Feb 2025 22:38:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f1386059fa17276f4f0e676f45370a63667006c4d8e514298f71c6639328ea`  
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea77ffafa6ef989339c5c391fb30729e3f148240c0834f1db148158ab32f657`  
		Last Modified: Fri, 14 Feb 2025 22:38:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f8ad18306ed8a7757d73f845d89b3aee98b4774af2b7c5c9a288bcf097036c`  
		Last Modified: Fri, 14 Feb 2025 22:38:37 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5c25f3816a63c8239c4a853ae22036406ffbd4f55b16e29e01f941f2dea356`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a329c61f9e1dc20260b65b0ef67440ced65fbf671c1e93df0a9710fbb42d536`  
		Last Modified: Sat, 15 Feb 2025 07:13:19 GMT  
		Size: 15.9 MB (15882642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5414ad0dfa4e22283cf2a1b5e1fbd9bf6e1d2b15db67b8c4f8aefd49fd514c`  
		Last Modified: Sat, 15 Feb 2025 13:00:34 GMT  
		Size: 12.8 MB (12773334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:5c6ec8183d52c07d4644f4b5b3ed8d6e27140f9253498e082e3408c1bccfec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1051334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe6b4e51b5dee39bf80278c1eb317f947ef3f4c26dbdd88c86c19b0018dc981`

```dockerfile
```

-	Layers:
	-	`sha256:64a36f780c9bcc9e22a670e18df188cb9a64f8061adaa5711048aba1ca3cf147`  
		Last Modified: Sat, 15 Feb 2025 12:50:26 GMT  
		Size: 1.0 MB (1029800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ac33fd2b22977af5b9b76398b90907296c788ae7850971285226bf9991a508`  
		Last Modified: Sat, 15 Feb 2025 12:50:27 GMT  
		Size: 21.5 KB (21534 bytes)  
		MIME: application/vnd.in-toto+json
