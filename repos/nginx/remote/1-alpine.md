## `nginx:1-alpine`

```console
$ docker pull nginx@sha256:4ff102c5d78d254a6f0da062b3cf39eaf07f01eec0927fd21e219d0af8bc0591
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

### `nginx:1-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:a71e0884a7f1192ecf5decf062b67d46b54ad63f0cc1b8aa7e705f739a97c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20810708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff4bb4faebcfb1f7e01144fa9904a570ab9bab88694457855feb6c6bba3fa07`
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

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:ade7925b79831f71093b59b1bb72a9ea194ddae56a7cb87979138f5a858c543b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **891.4 KB (891441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b42f035de27d7032d57b294a4c4ef856e9bb87d7c2ce9c369759ace36aed60`

```dockerfile
```

-	Layers:
	-	`sha256:68697693b101c5e762d51ec03fe6e00638c76b7efab149c91f90bc61ceba598d`  
		Last Modified: Sat, 15 Feb 2025 00:50:20 GMT  
		Size: 870.3 KB (870288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee2e1c0bab8bdb63e6ac974a37899c65717ed89a0a52ec9c4c2492489ad5cc3`  
		Last Modified: Sat, 15 Feb 2025 00:50:20 GMT  
		Size: 21.2 KB (21153 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:932b7633029fecd6580d86ec8c4ef44e700e539114d5a0fa2c2fe3c38948f690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18295508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f6e88a727dbbae3df0115fee9994fc800d705afe13ca81397de5eac91cae73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14aa9bdc206aa7a56d72a059b113bc82f9358c81f3bb61e2615904a3cb0c7d`  
		Last Modified: Fri, 14 Feb 2025 21:51:02 GMT  
		Size: 1.8 MB (1783055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b064f453733d00a4414e0e48672e817f402f60d4f1dc71ab51a145a43ca5e6`  
		Last Modified: Thu, 06 Feb 2025 04:00:19 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cebb56f31e960711f99cbf64861e06a184e857f5237250a7cae015796c55d7`  
		Last Modified: Fri, 14 Feb 2025 21:51:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b044c27b272687a3c5ab273fc6c5c9117ea7bb9a3d6eca76bdb48704a470590`  
		Last Modified: Fri, 14 Feb 2025 21:51:02 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b3c456e72829977ece6c04105ac791e716ad2de9570e7f0d3cb1a6b21d3dcf`  
		Last Modified: Fri, 14 Feb 2025 21:51:02 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a2d2d21b4755d8ea37aef87a01ca7716b6c0f6d5d2acf0ad5db64188eabf3c`  
		Last Modified: Fri, 14 Feb 2025 21:51:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a017f2c28e86220e7fe6fa581c4d374f17ae7462c73681653bb173a1fda93f5`  
		Last Modified: Sat, 15 Feb 2025 12:50:41 GMT  
		Size: 13.1 MB (13143115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:64f5d8bb1b874acf9151ae662b88b3d90f8457d6b84753e7cbf7219d0b6bf535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d355b1879ead1f28d88df4b7bf99aa80570e51d64ee4dc429d38a616783020`

```dockerfile
```

-	Layers:
	-	`sha256:9dcbfb1a28e3c9e35b3a9257810229bf1af2d5a1103b6092f4c52d87ee8d5554`  
		Last Modified: Sat, 15 Feb 2025 12:50:21 GMT  
		Size: 21.1 KB (21063 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:3e905249802061808f634e803c1d8fd28c029a26bacd296e14125248903cc4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18245557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02652123b7f32e5c61df5f497e26e601c47ed1a782220af9a201f7b7b58804e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8399da3a1b6248f570988fcf705376f299f760b7a835de5a20464219feba3abd`  
		Last Modified: Fri, 14 Feb 2025 22:00:28 GMT  
		Size: 1.6 MB (1618960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655e76109ae9f4555dd71bcd12240ef5a1736ef53bcdcfb1425015df457f5c6d`  
		Last Modified: Fri, 14 Feb 2025 22:00:29 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b39195a84e6603288b089f49f69472394f57343a433d120905f2d64c86d311d`  
		Last Modified: Fri, 14 Feb 2025 22:00:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9652cf2191508f0717e09c42545c7f69cc75e06a004271692200178a5665d6a`  
		Last Modified: Fri, 14 Feb 2025 22:00:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e922517595ce8dc944b395e805b4a329c36a1c469ae87b21198c3ab3f21a8727`  
		Last Modified: Fri, 14 Feb 2025 22:00:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d752c675767f1747f3925f2c2f55ef070b3ed93ff66170e6c9dda1927fa9156`  
		Last Modified: Fri, 14 Feb 2025 22:00:31 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752f5d89e7f2685ee31c86dac4b90713bbf5847d6091ded3d8a0828074dd949`  
		Last Modified: Sat, 15 Feb 2025 15:56:13 GMT  
		Size: 13.5 MB (13523870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:4f8d9401b4716a00982515cfc0bae83386ef6e40e4fe10b38fabb0500715cad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **894.5 KB (894463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d92f508cf4548c6ac8763452cc4698869a2a7a9aed497dd60bc0bdedd04711`

```dockerfile
```

-	Layers:
	-	`sha256:5f075c13ab89d8e47c2dc76df475c5deae2a79f2564fb4115a4d52601b65a88a`  
		Last Modified: Sat, 15 Feb 2025 15:50:23 GMT  
		Size: 873.2 KB (873185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd42fe4073ed1e5f1d39d3b0f22438f115c09dcde81fe6319fefb6bd5c3ae49`  
		Last Modified: Sat, 15 Feb 2025 15:50:24 GMT  
		Size: 21.3 KB (21278 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:56568860b56c0bc8099fe1b2d84f43a18939e217e6c619126214c0f71bc27626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21660647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedb667e1a7b4e6d843a4f74f1f2db0dac1c29b43978aa72dbae2193e3b8eea3`
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

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:e5239b390a6bdec21593fc5dff65e9cefa0eef5ff498b80f1dcd1c9f11ed431c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **891.7 KB (891745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb376b9963d4fd4ca97292e0e2b5656fa12e216296a19de0f4d0fee86b6b8d77`

```dockerfile
```

-	Layers:
	-	`sha256:980962469f77522596f29af1f2b8fcfcfbc0136f0fce8bfd26a9ccb269b7a042`  
		Last Modified: Sat, 15 Feb 2025 09:50:26 GMT  
		Size: 870.4 KB (870416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bf80a0f8d865a2520bbec67f22e5adbcca1f4d4b91ee672087d49f660e6dd1`  
		Last Modified: Sat, 15 Feb 2025 09:50:26 GMT  
		Size: 21.3 KB (21329 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; 386

```console
$ docker pull nginx@sha256:799a9c761078cbbd04bdef1f3578741455114a29c55988e697bfceb97fa14682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19869657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abab2f386031275bd565f0cb2f9d2f099fa9c3af897ea96b20766485ee96b98`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd9710d7c4f91680a1b139dfbefbe5b5d772a35decf8db284ed8c4bfaf9b536`  
		Last Modified: Fri, 14 Feb 2025 20:33:42 GMT  
		Size: 1.9 MB (1857537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2ec460bdf5babee56d7e13b060b308f42cbf2103f6665c349f0b98dac8962`  
		Last Modified: Fri, 14 Feb 2025 20:33:40 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c138d09b65aff69805299ed6ea5114754f3710ab0730dce79341cc657e4e94`  
		Last Modified: Fri, 14 Feb 2025 20:33:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f20665a341d3162ce5e0499c5c1556010462ad75c564f4388fe1eb9fa1b712a`  
		Last Modified: Fri, 14 Feb 2025 20:33:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8942d34d53f0016b507187729adac45417540d92e5facd09720fdcc07d8474c`  
		Last Modified: Fri, 14 Feb 2025 20:33:42 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dba93344ed20d492b4273939b2047c96688f9bf8b905a5b3601bf5925b643`  
		Last Modified: Fri, 14 Feb 2025 20:33:42 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2204af79066c35239ea1c7b30c00bf453ba7d6d9d2c4be8b36990df844c7f3b`  
		Last Modified: Fri, 14 Feb 2025 21:11:11 GMT  
		Size: 14.5 MB (14543909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:d65c5d0a83a2cbf203e5601f1f690088eace350396f4998f2e7fdcc7f62841e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **891.3 KB (891325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4647cf18834b405236cb96084938809874fada120e2ff5d0c638f3773009921`

```dockerfile
```

-	Layers:
	-	`sha256:297f670ea0019cf057628722325a1c56d51cae331950b271537a1ef117d3a217`  
		Last Modified: Fri, 14 Feb 2025 21:50:26 GMT  
		Size: 870.2 KB (870233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9285c4e8c2322193f23bf36e86f873c5782437a5fa5cf8fd75938394bf34aff`  
		Last Modified: Fri, 14 Feb 2025 21:50:26 GMT  
		Size: 21.1 KB (21092 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:5cc2bf1a5c61a392aa8782f2e8193e842702b003cadb31b917b183b46209da50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21379249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fade5b812fc49d96aebb8ff379387865e8d9a3441a2e7f3ddcb6878c2073c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea45b854f5d3d65710336824000538886e9cb992711e1022877fef48817e344`  
		Last Modified: Fri, 14 Feb 2025 22:00:42 GMT  
		Size: 1.9 MB (1852656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819fac15199237dd6eb7b359d9090a88b874516e6b7bf4487c145c9f2125a51c`  
		Last Modified: Fri, 14 Feb 2025 22:00:42 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce85edd0fe1fa8893a73f2e8af05f06a71dbb713b026322e9372431e11ee649`  
		Last Modified: Fri, 14 Feb 2025 22:00:43 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d223ae2386fdd3b33eda0a6df847b5768b612e854c22528d2fdab63cb8424e6c`  
		Last Modified: Fri, 14 Feb 2025 22:00:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190e0f04039d62732f4daa37d03e3a0f4f8714bb7e46c0d9f1207b120b64ecd`  
		Last Modified: Fri, 14 Feb 2025 22:00:45 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b57ddbd57987e456c8d6f00164aff25c53ebbf0432416fd1a969ccf813466`  
		Last Modified: Fri, 14 Feb 2025 22:00:45 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2063cd8c8afb2ea4521428e3de9d533c632fee0ca54937ab81b974e533ebc504`  
		Last Modified: Sat, 15 Feb 2025 03:52:15 GMT  
		Size: 15.9 MB (15947645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:d81c0c21c6ff4d97e136fd27b5ae357160c0ac7b9e7c4da7271e4585f1b546e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **889.6 KB (889640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b446e4d2aa5aac4c5e1787614c827efbd312a9f512cbc9a9539c861a5e8f63`

```dockerfile
```

-	Layers:
	-	`sha256:d466c8b81429f53c08591ccf41b7a7155d4731ff641d19039877f90856e4dfe3`  
		Last Modified: Sat, 15 Feb 2025 03:50:25 GMT  
		Size: 868.4 KB (868407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5bd9926ac429d3e341c9106765fe879c9dac23b85dce36958a2966464196bf`  
		Last Modified: Sat, 15 Feb 2025 03:50:25 GMT  
		Size: 21.2 KB (21233 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; riscv64

```console
$ docker pull nginx@sha256:1d07c11455284be0674572f7645a3ae637c9635d33273572f77b5984bee1a7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19187191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6e0e3b1d9c9aa04c6ede2f5687f31fb7317eb7e9ee27d7e07dca367d915168`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7200c499198f89b2dbba6097d8697f1cc3bc3c06136d273522b99c0de29f982`  
		Last Modified: Sat, 15 Feb 2025 01:00:28 GMT  
		Size: 1.8 MB (1825455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ae17ad953ff62072531b4b1d874b0ad0dfd5fbfd087a163d2e523bdd97583`  
		Last Modified: Fri, 14 Feb 2025 23:00:00 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6dde81d22d53ea75901a794c464442a5ca29da86a75ad5697b3b3d6082d7db`  
		Last Modified: Fri, 14 Feb 2025 23:00:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6295e7a7e6584aff50ef65f81b1bbdecd80a7003d77b2e294b1b1702312c2a`  
		Last Modified: Fri, 14 Feb 2025 23:00:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbd185d78455a9fdc66a514ef3a7afe20d74e19c1d737a48fc9b1f140e256b`  
		Last Modified: Fri, 14 Feb 2025 23:00:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa73c94d0aeafb21ff0929e6db9a086b16d8ac66888806e03735440a2e56b9`  
		Last Modified: Fri, 14 Feb 2025 23:00:11 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b0dcd399cec35b8199fd8e01d35f5949041e1c1d5d6833aef083e942cb92a2`  
		Last Modified: Sun, 16 Feb 2025 19:00:17 GMT  
		Size: 14.0 MB (14005694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:c9cec73c0a6427dc8481bfebce99fd2948cfca42d3e97be38a6b321f41f3cc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **889.6 KB (889637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425efedc098ccc4ec4b3185138c0ad2cc2b38985c43bedae79113cb0e83e81f5`

```dockerfile
```

-	Layers:
	-	`sha256:34221eddb0a82d8931368605a345abbb238b1116be523e5e3db2f64b1156cac9`  
		Last Modified: Sun, 16 Feb 2025 18:50:26 GMT  
		Size: 868.4 KB (868403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee12f39fbd6a79f029f40c0dbff7a5f8202c1bb3c7ddc81afe894fe3076008a`  
		Last Modified: Sun, 16 Feb 2025 18:50:26 GMT  
		Size: 21.2 KB (21234 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:ffa8132481ac1fae1948eea0d40a96013d385670dbf4e68c91127fa6e6eb0d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21456201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628950c219bb8a26fae6eca302a4cff24aa519c3e74e9b7bd20688b2652df8df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9e2cbbbd0b2be2ce5cff75d861930eb14127881af70499500f4d0ad5c9e1d`  
		Last Modified: Fri, 14 Feb 2025 22:00:50 GMT  
		Size: 1.9 MB (1886919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c030b62a00231dff47bf2c61f465580c49db2e1a564bc907ffa9383fdc193d3`  
		Last Modified: Fri, 14 Feb 2025 22:00:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc53039d32dcf7347cd8a3643b5be15797215ffa8dac44871e825095204d882`  
		Last Modified: Fri, 14 Feb 2025 22:00:52 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96885f6dd950d54e10a1e6964422ee6f07b306f7c8f1fad4800ff86221b5371c`  
		Last Modified: Fri, 14 Feb 2025 22:00:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d4c44054278c81d4939dedc85e26537db8f641ba0419e3d3bc3e2673bd025a`  
		Last Modified: Fri, 14 Feb 2025 22:00:53 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884de353fbcc3eeed5d0bd2e51059d4f10da8431d4236d6b9ea2ee94c64adca`  
		Last Modified: Fri, 14 Feb 2025 22:00:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99a1a6df8d4ad16155b41e3957f9f26277e7ff7961ec1f7c3c902d71063a739`  
		Last Modified: Sat, 15 Feb 2025 09:58:34 GMT  
		Size: 16.1 MB (16097116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:4b7dcc3ec2e89915ef193d026822d163bf6effeb975b8a7d196a3e7147a6c467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **889.5 KB (889491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f468b9589f62b30ad043a1e8284d919663ad9a250256445a4deb2d92905aeb7`

```dockerfile
```

-	Layers:
	-	`sha256:800c786de36062a9d7065bcad8bfac9f6b9aa51a2e8024dc51ff12f923b7baa7`  
		Last Modified: Sat, 15 Feb 2025 09:50:31 GMT  
		Size: 868.3 KB (868337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9973a016468e0fccb41f13e89e8a0bcfa5c05f9a5195cddd7e5e8b69e4c2d695`  
		Last Modified: Sat, 15 Feb 2025 09:50:31 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
