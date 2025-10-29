## `nginx:1-alpine-otel`

```console
$ docker pull nginx@sha256:0d8e87cc0627b84d505de78feaadc98981d80b45c1c2c0c21748c2f66b8bf77c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-alpine-otel` - linux; amd64

```console
$ docker pull nginx@sha256:3ed7dcd8fd1052d60d7c702fb72f5bde283589f56ac9c490d62429b6fca07ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36446896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780c034661764426fff1d70505a00ff9831e5ae7f4e40dd1bcf06d5eb7c727b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 21:49:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 28 Oct 2025 21:49:51 GMT
ENV NGINX_VERSION=1.29.3
# Tue, 28 Oct 2025 21:49:51 GMT
ENV PKG_RELEASE=1
# Tue, 28 Oct 2025 21:49:51 GMT
ENV DYNPKG_RELEASE=1
# Tue, 28 Oct 2025 21:49:51 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 28 Oct 2025 21:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 28 Oct 2025 21:49:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 21:49:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 28 Oct 2025 21:49:51 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 28 Oct 2025 22:11:24 GMT
ENV NJS_VERSION=0.9.4
# Tue, 28 Oct 2025 22:11:24 GMT
ENV NJS_RELEASE=1
# Tue, 28 Oct 2025 22:11:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 28 Oct 2025 22:25:23 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 28 Oct 2025 22:25:23 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"249858446828ace0c81ea3e057135aa368f3dab83430cf867bb9fc32598948f29c4bd50908491da704536af1106aa87553f6a76cc126c6833dc9b14dd00564b8 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6a6833e95d43ac524f1f9c5e7c1316c1f3b8e7ae5ba3db4e54b0c5b910e80a`  
		Last Modified: Tue, 28 Oct 2025 21:50:04 GMT  
		Size: 1.8 MB (1835502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194fa24e147df0010e146240d3b4bd25d04180c523dc717e4645b269991483e3`  
		Last Modified: Tue, 28 Oct 2025 21:50:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaba6cd10a374d9ed629c26d76a5258e20ddfa09fcef511c98aa620dcf3fae4`  
		Last Modified: Tue, 28 Oct 2025 21:50:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df413d6ebdc834bccf63178455d406c4d25e2c2d38d2c1ab79ee5494b18e5624`  
		Last Modified: Tue, 28 Oct 2025 21:50:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a55dab5954588333096b28b351999099bea5eb3c68c10e99f175b12c97198d`  
		Last Modified: Tue, 28 Oct 2025 21:50:04 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8a36d5502a57c3fc8eeff48e578ab433a03b1dd528992ba0d966ddf853309a`  
		Last Modified: Tue, 28 Oct 2025 21:50:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdabb0d442710d667f4fd871b5fd215cc2a430a95b192bc508bf945b8e60999b`  
		Last Modified: Tue, 28 Oct 2025 22:11:38 GMT  
		Size: 17.0 MB (16965479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f03dedbf6d00ae4ad96769235f9e9c0bd7b625866f5b4554edaf0705d1619`  
		Last Modified: Tue, 28 Oct 2025 22:25:38 GMT  
		Size: 13.8 MB (13838873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:278ee7a96709ee183b0df0dc6a4a356735bb644a82485c195b00ec0803578982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1082968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e300c2bdb015393c5a9a39de4b2f08d645e307ddcc947bb9bbb3345b6c8678`

```dockerfile
```

-	Layers:
	-	`sha256:67e11e439fa502035a8189abed75f98e9e5871341cbfed1175d45e7969f544d7`  
		Last Modified: Tue, 28 Oct 2025 23:51:03 GMT  
		Size: 1.1 MB (1061665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dadb12592addb5119738f789451fd7ab68a6b514cb8e0e7f2ad2a9ddd68c3454`  
		Last Modified: Tue, 28 Oct 2025 23:51:04 GMT  
		Size: 21.3 KB (21303 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:5c193bd7955cd7e1c32f5c6d394c53bc6c42df1b68c9903a71f8a5949f86e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36332254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399cfd812575ea22dce630bc6766f8aa58982f6949acbf8bab26b5cfa805bdf7`
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
ENV OTEL_VERSION=0.1.2
# Tue, 07 Oct 2025 21:06:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"633b2a8b56bd48527d7e293a255fd706dfbb5a9c47605ff18e91a2a409801043ee00ecb0da5fadf9cdf1d483c5ca848e81c1861870619523e15ca9e494b6e700 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
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
	-	`sha256:a0d4cf0de201e8e2a5a7b161c43ddb1378bf396cf6f5e399abaa6e520cdd7025`  
		Last Modified: Wed, 08 Oct 2025 23:22:36 GMT  
		Size: 13.3 MB (13277231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:865bde5ad584da5c7f4569675d2d645edc2f0c843567a60ed860bdd3f795b8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1083315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25617b5249f3f6f3e9d655bcf6db7f38f44a27aea6f0fd1132df2b90945617`

```dockerfile
```

-	Layers:
	-	`sha256:03561fdafe8cd960b9f46e68e27e5f0f80e6d1f2c3ea4e98e50e439d4c59f160`  
		Last Modified: Wed, 08 Oct 2025 23:50:40 GMT  
		Size: 1.1 MB (1061793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d3d3ae564f00a21a610455d6a74fce48ac977373e2a334f7d790d141c5fba0`  
		Last Modified: Wed, 08 Oct 2025 23:50:41 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json
