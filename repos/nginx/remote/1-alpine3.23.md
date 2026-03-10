## `nginx:1-alpine3.23`

```console
$ docker pull nginx@sha256:1eff5a5f3fcf8431a0abb7eddf5471fec24e5e1905a2581aeacdb07a4479b92b
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

### `nginx:1-alpine3.23` - linux; amd64

```console
$ docker pull nginx@sha256:123827f4a105eee4054d59a0080f7860b2a7e29fe138d132af7850843b54c833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25963149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274331e2723726d667f697a57a67a709549aa43f62a6742510967a934a62dcea`
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

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:b3c0f1953ce5f30a480b0a34fdce2e76c1a30ddfcc4b228676ca9cd97c7f00cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.7 KB (909663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e48b401100908faf220ac4c6cafd417490b2896f634a29fb911b589673cf4b3`

```dockerfile
```

-	Layers:
	-	`sha256:c2d2ef765a7b6f991b4ce52c18cf84be9174ef8545d1fad243ff4e965aef31a2`  
		Last Modified: Tue, 10 Mar 2026 21:11:21 GMT  
		Size: 887.1 KB (887128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e48b3bd2071cfee3641e691b198e552de4014d8d967bcfcc942b1f6d41f51a`  
		Last Modified: Tue, 10 Mar 2026 21:11:21 GMT  
		Size: 22.5 KB (22535 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull nginx@sha256:2a2ce5294a38652ec9f15cabec38c2b030ee7360fcccb848affd4426942abe45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19675045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba40e9f4d08562be0ca4ea648cc29596416aafd3a2bd72796fc669145077dc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 21:07:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 21:07:31 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 21:07:31 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 21:07:31 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 21:07:31 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:07:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 21:07:31 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 21:07:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 21:07:31 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:20:36 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:20:36 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:20:36 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:20:36 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd81141dbc3ff87dd297214f1f73f1ad8bbb4009114e9802e55238a48ed56bc`  
		Last Modified: Tue, 10 Mar 2026 21:07:35 GMT  
		Size: 1.9 MB (1902997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93facf12bc39eee3b2f017eaa71e2940f42ea30bf3ee2c56bafea66c772f3e`  
		Last Modified: Tue, 10 Mar 2026 21:07:35 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3b3e95ac6b3adf54298b6763db4be806237f72a1d0eb3cdbf52cbd35bbea88`  
		Last Modified: Tue, 10 Mar 2026 21:07:35 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aa4ccd46680f748cdfaaef101005b1e7af5d54db97af1e29eabe3fc0cf142b`  
		Last Modified: Tue, 10 Mar 2026 21:07:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed23c2887ab566c5c54875d3e3b50c72ca848c38120eabd79b1818453be945f6`  
		Last Modified: Tue, 10 Mar 2026 21:07:36 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc163b3ae09d6f3c51251fd229127434d67840b2cb90960026d2bbae3c3d0a`  
		Last Modified: Tue, 10 Mar 2026 21:07:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cbe965af958f9964b133e845a4a4fc14acec1d11d8333c0c7ddd2542ea3b70`  
		Last Modified: Tue, 10 Mar 2026 21:20:41 GMT  
		Size: 14.2 MB (14197627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:c8221cff5a3c31aa0a2f2e9e5e6d158ff7bd7d5cef3fac92efaa1d37c580a7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 KB (22449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbebc63e8ab15b217ec52d3539192351b91af27e2469863cc9714aaeded18c`

```dockerfile
```

-	Layers:
	-	`sha256:835b6a902f269a4b027b00b81ddc77e87f6749c0051f3d1d5da8088e9f800334`  
		Last Modified: Tue, 10 Mar 2026 21:20:41 GMT  
		Size: 22.4 KB (22449 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull nginx@sha256:dfb628c672f0ab395ca495dad2ae1f6da0126d045be5575b286ca8d6f857bf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21649779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f40b2df718e58fcd56e3348b32d39eafc89834fbf82d98c9dd6ac9b8fd837a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:53:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:53:31 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:53:31 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:53:31 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:53:31 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:53:31 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:53:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:53:31 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:13:59 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:13:59 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:13:59 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:13:59 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d824cfa187b361d45e54c34f9733d9eb1954752ee431d29b890fe828758dc91c`  
		Last Modified: Tue, 10 Mar 2026 20:53:36 GMT  
		Size: 1.7 MB (1726085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44d5e4fec8a72e933c8fa10a0ecf2e767f98b946ecf11e4d179683cafd1a8a4`  
		Last Modified: Tue, 10 Mar 2026 20:53:36 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab311afbd93703dd22653de4a2ebb7e01acc881003ba850d06b63081008fa1a`  
		Last Modified: Tue, 10 Mar 2026 20:53:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93281b3f3cce83ef71636a3e8df89c46891fab171b402dd67587929f9e2f3177`  
		Last Modified: Tue, 10 Mar 2026 20:53:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b31ce6646df7f8bf1ec9e11273b1082ed6d5ca7e3744738dc2e06df64ce82c`  
		Last Modified: Tue, 10 Mar 2026 20:53:37 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d0716debee3e4ce5144f36c977f8a4373be141a95c29f7753866e8825bd7fd`  
		Last Modified: Tue, 10 Mar 2026 20:53:37 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d56e7747ba476a4119f6751e92e880e50b3bb6e041a2b93a7a4adfaa5e201`  
		Last Modified: Tue, 10 Mar 2026 21:14:05 GMT  
		Size: 16.6 MB (16637377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:535113f4b8f782863b453fd0bf0917815457dd35625782f3c1d47e03309476c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.2 KB (909226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f0bbe932bb80cc2a60fe1aa1367965859fd270a1d41a6db82452c5aee446a`

```dockerfile
```

-	Layers:
	-	`sha256:65258490913359f07cb4bf5833b57fafe700daa40c03ea85716a5407c2b2bb86`  
		Last Modified: Tue, 10 Mar 2026 21:14:05 GMT  
		Size: 886.6 KB (886562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de255bff91c5087d10a24d95c0b290ec37cda28221aba264216999b0b82bd91`  
		Last Modified: Tue, 10 Mar 2026 21:14:05 GMT  
		Size: 22.7 KB (22664 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:fcd2f0ad6349997f7e2d7574364deb032b584ec57db6793ce44438d3bbf0ea54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25786936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f86deeeaf87a192af32dae6e786e810adbd711a25e1c2c6bcb6d72d77e2a6f`
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

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:b91f359eed5e8bd10ce15ef86b5cee46c6bcfa4fb0261088f78ee3f020416360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.3 KB (909317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dacaaa7bf774990c1d14f514b8d2757a5cc7d556eaa6d248ab2bab883ba572`

```dockerfile
```

-	Layers:
	-	`sha256:64469660d2ff005d5a521287952b25d5c16f3d7b1f763290ab9289a734bc23ce`  
		Last Modified: Tue, 10 Mar 2026 21:22:14 GMT  
		Size: 886.6 KB (886606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af250218d167a830a269cdbe2ed2ed3baca93df65d362aa69169f86844c8f9f`  
		Last Modified: Tue, 10 Mar 2026 21:22:14 GMT  
		Size: 22.7 KB (22711 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; 386

```console
$ docker pull nginx@sha256:b310c35c97287673b8e2e032eaf49ccf608362938391b7592df941d76c602c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25315888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e9814497fd62c9a3d3be942beea01583632a49e6a832957d0391c01fa6af1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:52:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:52:45 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:52:45 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:52:45 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:52:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:52:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:52:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:52:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:17:36 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:17:36 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:17:36 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:17:36 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cc269d23acd809b2d04bee2214a459f9894b28007ca45178097a84032e05a1`  
		Last Modified: Tue, 10 Mar 2026 20:52:50 GMT  
		Size: 2.0 MB (1985125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d81a5408b862afeda01f91bb2c8acf21183410ddf9fb207d750ba7131014068`  
		Last Modified: Tue, 10 Mar 2026 20:52:50 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967d0e66aadd37bf1f36d911ab51bf25e8913bf5479a40610891e6a01279b01`  
		Last Modified: Tue, 10 Mar 2026 20:52:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683b2e33d65388ac31c666d0efd14bdb0fc06712dc51a6aa81e5dd6be8249f7e`  
		Last Modified: Tue, 10 Mar 2026 20:52:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da80fbeb89244bca245f18ccab84ceb052c30d02f612cb1658488f730169df97`  
		Last Modified: Tue, 10 Mar 2026 20:52:51 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943038f1b8f2d731de3441efc75f1f131873bac919dda5a484b3d1185f784ea`  
		Last Modified: Tue, 10 Mar 2026 20:52:51 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f1a485c337ef64646f90259b35b7fdfb12b8f52b0fab572966f01e315ddfcb`  
		Last Modified: Tue, 10 Mar 2026 21:17:43 GMT  
		Size: 19.6 MB (19639176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:ee84df6293afccd5033cc58af2f3736345fac31c30adca1e2ae14bd6b4b98220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.5 KB (909547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b9281cc201957d427adad0740b9293b3ede97a27d7dce46d2df7c66d6a4922`

```dockerfile
```

-	Layers:
	-	`sha256:54789b873ea450a63742af276c8336e3c3ef279f59d5e5188d6e3fbda0b1be40`  
		Last Modified: Tue, 10 Mar 2026 21:17:43 GMT  
		Size: 887.1 KB (887073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9b7e3bc47f4bcdf3fb74ffa38b0bcdba90d2482f1d0640a327cd5b3f2f9ad9`  
		Last Modified: Tue, 10 Mar 2026 21:17:43 GMT  
		Size: 22.5 KB (22474 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; ppc64le

```console
$ docker pull nginx@sha256:8c5254d26e35f8b50b67ba580288f66f8d98e3317c9c30bd41c881d72a5e1766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26341353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2597c2339a09b886f06230bd69b3ee01461afdf3944a8ee20f48ab7a3c2da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:47 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:47 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:51:47 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:47 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:47 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:50 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:16:20 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:16:20 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:16:20 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:16:20 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ef4d57f0a9496f7adf8a20c3acfaeed63d9c99ff21c5d2258b443bb4ce15bf`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 2.0 MB (2006952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54deaa7e4b3af2c8cd11d21521e24780ff398b5b1fd699c833f08e5f8825728c`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433354bc719cb05eb364375f0ccc44ba545153e54bba27f0d5295b1f9a4dfea9`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d31fa12304ea13bd49d156b594d9ae1c859e266af556760878c5e4743284597`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d99a5e768b381a5b11cc629719359a6f32c0370c725f3c9ac6db93120cee3`  
		Last Modified: Tue, 10 Mar 2026 20:52:05 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c22d58a6d989838fff142f9ef8f4b25cb4a07aaf481cd4326872e67dae5b8cd`  
		Last Modified: Tue, 10 Mar 2026 20:52:05 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bfcda60aa65cd73feaeb29d4b851da1c83df3d8bfb24e870c667432dfc65ca`  
		Last Modified: Tue, 10 Mar 2026 21:16:38 GMT  
		Size: 20.5 MB (20500165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:694c638786ec4868b49a63f02898aded4acf07ceb8ae1105855df03ad67412c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.2 KB (909163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0b0615c6825af82aff974a264de820288ef2a923110363fb076992d79f72e2`

```dockerfile
```

-	Layers:
	-	`sha256:1c6037c1b243cc2da172f4c4fa4fd0e7fedc61faa89af60cf4db58bebebf79c1`  
		Last Modified: Tue, 10 Mar 2026 21:16:37 GMT  
		Size: 886.5 KB (886547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85835d64ecdaff58b1ccfb82a1f0d870e76f87ae8815cc84b0c6cbd0d051db0f`  
		Last Modified: Tue, 10 Mar 2026 21:16:37 GMT  
		Size: 22.6 KB (22616 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; riscv64

```console
$ docker pull nginx@sha256:16b6d095ffa1be76073ae41c3d0735decd311fd355ce8dad516e49e7df7b8e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23485662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed01d490238cfccfb369b699b26084da167921697ccc7e3e73080db21d69e236`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Feb 2026 01:10:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 06 Feb 2026 01:10:27 GMT
ENV NGINX_VERSION=1.29.5
# Fri, 06 Feb 2026 01:10:27 GMT
ENV PKG_RELEASE=1
# Fri, 06 Feb 2026 01:10:27 GMT
ENV DYNPKG_RELEASE=1
# Fri, 06 Feb 2026 01:10:27 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 01:10:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Feb 2026 01:10:28 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 01:10:28 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 01:10:28 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 01:10:28 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 01:10:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Feb 2026 01:10:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Feb 2026 01:10:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Feb 2026 01:10:28 GMT
CMD ["nginx" "-g" "daemon off;"]
# Sat, 07 Feb 2026 20:53:38 GMT
ENV NJS_VERSION=0.9.5
# Sat, 07 Feb 2026 20:53:38 GMT
ENV NJS_RELEASE=1
# Sat, 07 Feb 2026 20:53:38 GMT
ENV ACME_VERSION=0.3.1
# Sat, 07 Feb 2026 20:53:38 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc71149aa9b4d1e53e27373e3f2a27b391420ba2b67c52c7fd6c7caae85c4c1a`  
		Last Modified: Fri, 06 Feb 2026 01:10:54 GMT  
		Size: 1.9 MB (1899460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4da95ddbe6bd43751ef4a8168e519623128dd8b30b300221fad53d9328a8ca`  
		Last Modified: Fri, 06 Feb 2026 01:10:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b355712486e7e8aad31c3186673656305b60fb4b696463b4574bdd29f7fbde3`  
		Last Modified: Fri, 06 Feb 2026 01:10:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed9a46d02d719fda5fd46975ff5ad165ed1f5ab40291e7e9bc0f5d3a318e4b`  
		Last Modified: Fri, 06 Feb 2026 01:10:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b315aa757be8d8ba8f5b92f38d387d2d2b983369f6a77328caa25cc42e9d33e9`  
		Last Modified: Fri, 06 Feb 2026 01:10:54 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab6aa92b471835683671fe9d883bde91981793581d3710d9317ae9dc958930f`  
		Last Modified: Fri, 06 Feb 2026 01:10:54 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebcd3d195d1063fe4bd743cc0f685fa8cebe196139bb4d70149c9ccf5152020`  
		Last Modified: Sat, 07 Feb 2026 20:54:30 GMT  
		Size: 18.0 MB (17996319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:c71fee77b6b881a19626d5163ff80dd5dcdb11194ba700bc638c88b6ea0df974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.2 KB (909159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de598178963f924872909523cc6441a1fc3dd9977ccf1b3abc82bc137db25c6c`

```dockerfile
```

-	Layers:
	-	`sha256:0214ed68e27a46119a3e23d3050fe5717a7973d590b11d04bbac34f683175a8d`  
		Last Modified: Sat, 07 Feb 2026 20:54:26 GMT  
		Size: 886.5 KB (886543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8188e6e9526c7a5c27b977bc0e08f4825b2f224f922347b2a6033ecbf13c8d8c`  
		Last Modified: Sat, 07 Feb 2026 20:54:26 GMT  
		Size: 22.6 KB (22616 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.23` - linux; s390x

```console
$ docker pull nginx@sha256:a999f72db2a0f144c000354cc70c02383d824ea9a4e1caa241fb832ac5729bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26116637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9ec1a4f3acd256d9816671a8679a5676da12ec284b67630452410fbc7dd84d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:34 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 10 Mar 2026 20:51:34 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:34 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:34 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:34 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:13:32 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:13:32 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:13:32 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:13:32 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98ff2bf749e6e16ad3af3a587083c001114e82d26477da52dd3d36778139a1c`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 2.0 MB (2030832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb7062a534a98ce64541e0ecb3c011d8b1c0599d3ada2095795703b150cdbe`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d20afb7ced6f48739b1a036cc7cb2742935496a440287a960f6224b4c5a4de`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fd66fee56e31615a7699ff34446f497ec204a98d2ee7ef77aeea473509c538`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970f64ca9139cad9347073e8f99b7877f40ff036468afd46033a79846c194886`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb16e37ebadf35261d49389650fc7a0bb17c17edf94c16ff69089597d4d236b`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccff26fbc06469589e523a6ce461f87aa489146c966177e31f901645e9935e0a`  
		Last Modified: Tue, 10 Mar 2026 21:13:46 GMT  
		Size: 20.4 MB (20355881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:b5bce42f167e3669f960b0c879f478713c445dbc5c3816f93429a9116785f190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.0 KB (909012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7152309248b69b1474d2a41016e4108779c875255ea79bfc12093c5475f502db`

```dockerfile
```

-	Layers:
	-	`sha256:1ddab0cf747ef3948e7162a13ae97e073b2d7b009dbd11625c0fa96dfc78c857`  
		Last Modified: Tue, 10 Mar 2026 21:13:45 GMT  
		Size: 886.5 KB (886477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cb3472321b0ee094f6750e91d1a85d52ade041c547b3d75187eec2f8f359bc`  
		Last Modified: Tue, 10 Mar 2026 21:13:45 GMT  
		Size: 22.5 KB (22535 bytes)  
		MIME: application/vnd.in-toto+json
