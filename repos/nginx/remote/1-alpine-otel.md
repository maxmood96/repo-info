## `nginx:1-alpine-otel`

```console
$ docker pull nginx@sha256:37f08a8dfbd3e19032794ceb81b3e805b1247e91c30192321581e97c94bdaf8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-alpine-otel` - linux; amd64

```console
$ docker pull nginx@sha256:61a443a3369bd0e8796f55aace42132f426ef505190793667298275500d129a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42721092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d64d28f8969e43450c09cc40b6a28a327a07fa5295db8b244e66b75d22c9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:39 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:51:39 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:39 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:39 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:39 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:39 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:11:14 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:11:14 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:11:14 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:11:14 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 10 Mar 2026 21:38:08 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 10 Mar 2026 21:38:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565dcd14d83b19745c95328eb7c3cc798f677d35eb19aaaf930d21d2f0674999`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 1.9 MB (1856075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7323cfb6ecc33af8861cdbf915e9cd25d5040970622c58d3ccee2a28f537da9`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505610f0847fc55d522cbeab5cc38bd5b4e6db6454585e0375e7de78d4feb020`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57772a2914efea6dac5cc146369a161e10a56d7242c89cd3ea2b69723e2948f`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff6f2f31a3ccec2bdd8d016e30d28b2509c11e1893ec4b399fc3c1d86326211`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c331179be97ce2834fbaf5b9ff4814fc90c516d270e33fb903dae958767b28`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ebc4ca7c9ab451636fc4895c655bf5c1ac72e8b3d6632948de08b97b2c3b87`  
		Last Modified: Tue, 10 Mar 2026 21:11:21 GMT  
		Size: 20.2 MB (20240662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17f9b7d9d148d365d204cecec2e84e757209872853d6fffa130c9c058408352`  
		Last Modified: Tue, 10 Mar 2026 21:38:16 GMT  
		Size: 16.8 MB (16757943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:ba35d08f9b2744c14bc7334fb616bd07616b5196ff99c5671eebebed0927a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1097501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e4201a211f7ca71a76c09a2ee1145936fd5ea0c3f037c46be1b291d25755fa`

```dockerfile
```

-	Layers:
	-	`sha256:1367e6991da3c0aae46d260c6d334a6581b3419e341abc6e5338adefdbe33f60`  
		Last Modified: Tue, 10 Mar 2026 21:38:15 GMT  
		Size: 1.1 MB (1075958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bddd12a95a82dbd3b5630ab932fef943fc2555034626fdba1a25e0b9dce1e8f`  
		Last Modified: Tue, 10 Mar 2026 21:38:15 GMT  
		Size: 21.5 KB (21543 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:25c40e05354cd886f21c37e51b2476764163e5253cac18daa3db7170e8e0a657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41518441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de31dcab194ad6556cbc8b09486e7c784feae1a130642105efc7e7c4802068c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:54 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:54 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:51:54 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:54 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:54 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:54 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:54 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:54 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:55 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:55 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:55 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:22:08 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:22:08 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:22:08 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:22:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 10 Mar 2026 21:38:14 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 10 Mar 2026 21:38:14 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1dc3dc52cd1bfa3f1e872d9c08f28ef4f7757781e19701313f16c9c8d1c529`  
		Last Modified: Tue, 10 Mar 2026 20:52:00 GMT  
		Size: 1.9 MB (1873423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40280dcfb80ad8f91fe30957d07ba2901bb79b8c56a9b081ff8b32fbb3247484`  
		Last Modified: Tue, 10 Mar 2026 20:51:59 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79832e474b3ad906aaa027218b75e1c066dbc924e9108a18afee637cd08fa85a`  
		Last Modified: Tue, 10 Mar 2026 20:52:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe8733124a5b364267713e8f39c0c4c4b28a38a04a244007f5dcd0938b7477f`  
		Last Modified: Tue, 10 Mar 2026 20:52:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6979619db6443b260d507e34b189bd16609263299767ee0a55e207bdcbe980`  
		Last Modified: Tue, 10 Mar 2026 20:52:01 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b49ebbaa896e6a2edfe20c58964e1ed743ae7ca72df427a9dcc84dd601eafef`  
		Last Modified: Tue, 10 Mar 2026 20:52:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bc77c0cf17c9cd5505be48c2ade35428d3f8f845fd5e714cd27c3c3f5d937`  
		Last Modified: Tue, 10 Mar 2026 21:22:15 GMT  
		Size: 19.7 MB (19711831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf3136b1070b867cf6abe1f386db8e1d50a6b59943c984f8e6303cfddc4ec4c`  
		Last Modified: Tue, 10 Mar 2026 21:38:21 GMT  
		Size: 15.7 MB (15731505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:31f07b934f31cb165863bcea2cb78b5a363a333d76c0df3f659eccbfb556d119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1097155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e2b68842767e23f0c071591e367d46482c7907ca706fb37c1c62f6a876215c`

```dockerfile
```

-	Layers:
	-	`sha256:950a9310a4883900ba7928c3027bb2675de19ee10c0db6a17bf565013ac037e8`  
		Last Modified: Tue, 10 Mar 2026 21:38:21 GMT  
		Size: 1.1 MB (1075436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8b19302ea83e1cf1a40ba050fa252dd73a40dbdf98cf55a6e11e473fe5b1d3`  
		Last Modified: Tue, 10 Mar 2026 21:38:21 GMT  
		Size: 21.7 KB (21719 bytes)  
		MIME: application/vnd.in-toto+json
