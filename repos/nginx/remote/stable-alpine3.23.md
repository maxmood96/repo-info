## `nginx:stable-alpine3.23`

```console
$ docker pull nginx@sha256:8947b9864b3ebbce6f14bcc1605158578125251b179d2dcaa6d407ef398f25c4
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

### `nginx:stable-alpine3.23` - linux; amd64

```console
$ docker pull nginx@sha256:83902b81d5d0ebfa863977a4ae2260c18bee6817fae0e534c57cab0c1d584a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26019805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7afdc84df3e03abaf067384e862a08cb7204bd6ad202e91bb59a2fb8a21e5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:25:13 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:25:13 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:25:13 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:25:13 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:25:13 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:25:13 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:13 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:13 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:25:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:25:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:25:13 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:31:01 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:31:01 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:31:01 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:31:01 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591de949fc47baa1d06c6e76fd2e31bb74036616af82eb8f8f1587b3ea79c2f`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 1.9 MB (1870854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e17fbea4a6e1edc792689241b257ca92f5cc662ffeac9cf227e71357df7ba3`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b5c71f63d4bdbecf7e4cb43b0241dde98e03b04af058eb54c4e155987d855`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db114418873157bc8c284b9f6da6dea4c1bc08c80fb4c490f45a12ede8c2ede`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36afaf6978329f60deb48adb5d35635fd89334204776fe93c2f548a178ba6472`  
		Last Modified: Fri, 22 May 2026 18:25:19 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1872bceaab57004b3b89c6ee3755c3386063852cfc9c5ff68245417047cdd2`  
		Last Modified: Fri, 22 May 2026 18:25:20 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b009abd4e3ad8c26f28dac7b863c357bd87148a3eb023e8cdf08403e457ed87b`  
		Last Modified: Fri, 22 May 2026 18:31:09 GMT  
		Size: 20.3 MB (20280168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:866f7483a52d1150507e9f8947960255f5c3fcfae09c17155586132383851e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.8 KB (903763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f7fc056ced88914e38970bc4bdcf58dee5c701f5c79d8e9ce85d590f8d0de`

```dockerfile
```

-	Layers:
	-	`sha256:3fda7ca4bac672ca2c50cd8adf437f4ff2f9685f65ad58ddc7fd7391f6c9a4d7`  
		Last Modified: Fri, 22 May 2026 18:31:08 GMT  
		Size: 882.4 KB (882363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a81e560497f5351115517ad0d49fbaed116d286ccd1ecee2c1a9b879ef57820`  
		Last Modified: Fri, 22 May 2026 18:31:08 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm variant v6

```console
$ docker pull nginx@sha256:18a9fb2326afab690d1362fa5b5992fffcc4cf7b61da2124f949b380598f9e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19585852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c086df632ce7a0ba31a548e8be8f381031c6c6706753e26de41f864e2551a84d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:24:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:48 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:24:48 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:24:48 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:24:48 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:49 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:29:08 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:29:08 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:29:08 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:29:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6eb260e9b5754210ce374bab3bbf1c3aff0aed45cf31190e170b18c60fd2b0`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 1.9 MB (1868365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc897814cd63894dffe331b48c925a4cf4c84a2bf2ec9f2c64a322550a67912b`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74021b1808429847bbe6c3904e2ee1684f94399669d9c0eabf20ccc7e680ad48`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4316aa51d925d1e29bf2c42025d3defcb0eeabb1ecc6cc49de1218cb62391c9f`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eabbe58c39edaf88b3c74e27f8968eb33aa53b272fd3d323a4fc7a29d05136`  
		Last Modified: Fri, 22 May 2026 18:24:54 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a9d6ad4fadef3719a8ca9b5fdf2322a64f315faff5e2cb3cc47e411deadcec`  
		Last Modified: Fri, 22 May 2026 18:24:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5a66198545cdb16d6fa50707197523b3723febfb15e95ea30394f152422d4b`  
		Last Modified: Fri, 22 May 2026 18:29:14 GMT  
		Size: 14.1 MB (14141027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:31ffe55b440b56fe8550fd62815c3f9c24d0ca8293018fb69705357359dda914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 KB (21281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650ba81baeb63fa7d78d6034f1d0e07d9d79583abda3a4135b9cfd173faf77ca`

```dockerfile
```

-	Layers:
	-	`sha256:abe045e9fdd6f2c30c504238df9647c7d8d18971b954b4b7f5dffe527e8fff0c`  
		Last Modified: Fri, 22 May 2026 18:29:13 GMT  
		Size: 21.3 KB (21281 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm variant v7

```console
$ docker pull nginx@sha256:707bfc18d71f9907d934026eff58b00d25b336c349dc8a9e42c654ea43756e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21635966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6d5b2aaca48784cc55499542893a7ad7714f5e05db75be9667d7bb57f3cf9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:26:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:26:26 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:26:26 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:26:26 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:26:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:26:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:26:26 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:26:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:26:26 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:38:50 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:38:50 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:38:50 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:38:50 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41868c36b2f00814216181d3e3c3d5d3081221dbc3c0e0a793609df9b35fb894`  
		Last Modified: Fri, 22 May 2026 18:26:32 GMT  
		Size: 1.7 MB (1693789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b196b311f587c629cc4b6dc54300cb9f80ea1ea566e99f660c788ededafeb78`  
		Last Modified: Fri, 22 May 2026 18:26:32 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a821be167b2040c0eec4ab1a9f99930b4d28bcdf61e13a3d148c24fbe5a9c63e`  
		Last Modified: Fri, 22 May 2026 18:26:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8b6c55164c5d319dc1c3d80a52c15f7b37b28a111da338b11716d9fc0547e`  
		Last Modified: Fri, 22 May 2026 18:26:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d4dae08c86d2f184f4a38a215bb278da82ffbb20bd325d71e6cfe700e9b53d`  
		Last Modified: Fri, 22 May 2026 18:26:33 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5070aa280ca410befac83f815462fb493774e7decd7f898a00452923cc717a3e`  
		Last Modified: Fri, 22 May 2026 18:26:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe46308ef7228c42cae5bd40ead6f1d6bed335fb423c1460799a53a344d1645`  
		Last Modified: Fri, 22 May 2026 18:38:57 GMT  
		Size: 16.7 MB (16654456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:9b1462f51193b7afc7696433411b8fbec3cb65685a9883f789cf8211587a586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.3 KB (903261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553180d5f33d9adefdd8dbd2e80b0b13a36123c1d2962747aae90e2b8329b2e7`

```dockerfile
```

-	Layers:
	-	`sha256:8cf21e05fa582213a58c70a23e9589a8b8c142540b80976a5e29abb1e68d937d`  
		Last Modified: Fri, 22 May 2026 18:38:56 GMT  
		Size: 881.8 KB (881765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe05fe25c3f66910eada42ac9794ad747929d48a616722f7108dcbf00e2641f`  
		Last Modified: Fri, 22 May 2026 18:38:56 GMT  
		Size: 21.5 KB (21496 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:cb13fe7d2a995e6bce2c3182a6a0b95fa0622534417d5b92c7c883e28cab48f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25823233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c59af5e22f7974252e866c5347a056bf519d41d8551f926f9bf855d148c5fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:24:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:44 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:24:44 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:24:44 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:24:44 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:44 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:26:21 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:26:21 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:26:21 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:26:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eeda869ba1f71ec25843c77bedd1ed161f244e20f9e34649c89eef6a7cfb26`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 1.9 MB (1891358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbbdc4b9230ad0e344fdfaf6c610be06abd8f8b5c299e027a51f4da6751cb1b`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77ff2fd3eb3c1ba3bbe79d903dccefbc4878310a44bf1c3462c79ed1b79bd9c`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f4da3cdb6eb3330aa6e4be1cc7c8853c5008b03315a7413d4239d19cfa6eb`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6e64485597605500cbbf14827bc56c589b134fe9ac1ed10d54028ebba9c3f4`  
		Last Modified: Fri, 22 May 2026 18:24:50 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea3fdae34707bf56f738169361c460571f7bca3bebcc2fb92ac28180608e0c6`  
		Last Modified: Fri, 22 May 2026 18:24:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a6cd5ad95a25f0842fa56b5563e658ac9331343a1d691551fe148bad584fd`  
		Last Modified: Fri, 22 May 2026 18:26:29 GMT  
		Size: 19.7 MB (19727420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:30b76370fbf3927ecf2868c7ddc3c6ff68bee2f13bae50da6873cd8247eb4da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.3 KB (903321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93360e9720e77e0ecdc6f362ed19d574535431e0c974261d27fd60828975bbe`

```dockerfile
```

-	Layers:
	-	`sha256:3e11cfd6691cfdcd345d6edbe7a750b7ae1d8d2f71e08559bcec34eaf3b54c27`  
		Last Modified: Fri, 22 May 2026 18:26:28 GMT  
		Size: 881.8 KB (881793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23de84aae652fa1a7fb9111aee2fa01614aa7d6ab290a4c7f13cb71f214330cc`  
		Last Modified: Fri, 22 May 2026 18:26:28 GMT  
		Size: 21.5 KB (21528 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; 386

```console
$ docker pull nginx@sha256:7390e25a11474d8ce30e8b458289117c17c9fc07ece236204533c22070c4305b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25302244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167cea161e2fd3e00c1ea58cd4ddccf52368c06bf6fbe26314009534bdc39f93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:26:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:26:45 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:26:45 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:26:45 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:26:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:26:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:26:45 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:26:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:26:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:38:22 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:38:22 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:38:22 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:38:22 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee12bdda6b1dacd6500e299c29cddc6cce480eac98323606cdf53813a501afe`  
		Last Modified: Fri, 22 May 2026 18:26:50 GMT  
		Size: 1.9 MB (1944574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de5116e88b268d1e7c9e85e8cbe7c95d7c3322852606a62878df84fd78388c1`  
		Last Modified: Fri, 22 May 2026 18:26:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35222c611f2c4b39f21d1eda56ffdaf69f8e5d109b0043a32c3f8896745d1e46`  
		Last Modified: Fri, 22 May 2026 18:26:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b5e041447c07aa529c578c0e9e53b90f2f10446bac1217c6d7edded9339a4`  
		Last Modified: Fri, 22 May 2026 18:26:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177ba6f89324b22995bb18585a6a3c137dfe9c28bf4d8474a4f6efe127ec610`  
		Last Modified: Fri, 22 May 2026 18:26:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377339cb2b4f1455b890361e7fc8c5fcc9dc28e5d68a80042ce7b09a4467f2c9`  
		Last Modified: Fri, 22 May 2026 18:26:51 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441b9deb6cd27b2e86016df0b335fd6c6788e2dae354e6970359747eb46a6e7`  
		Last Modified: Fri, 22 May 2026 18:38:29 GMT  
		Size: 19.7 MB (19662624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:a02096abff44f59d3b84e5dbbd2cadb8c77707ccfee596e95d81523f2cd538b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.7 KB (903686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e49a1133a6b7986dacd06c1c4de2c824e0adf50886446311474b69b9a1d2f1`

```dockerfile
```

-	Layers:
	-	`sha256:d257233850afbbb27e42a2ce6741c97d03981285b3ed252f73adf8b7c9708a5f`  
		Last Modified: Fri, 22 May 2026 18:38:29 GMT  
		Size: 882.3 KB (882328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a147c544cf8bf42f307c65a9c6d65e90dc16a0cf608958b37cd973cc8db707`  
		Last Modified: Fri, 22 May 2026 18:38:29 GMT  
		Size: 21.4 KB (21358 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; ppc64le

```console
$ docker pull nginx@sha256:c20e7bd47ea05f0ced9a9f49fc8fc452cbcadbe7d1a14e4681aa6b535f9ab701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26319171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7a18a0b1f68a0bb10868313184bac82e00c85c8fe3a86289ceec5c8695552d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:30:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:30:20 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:30:20 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:30:20 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:30:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:30:21 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:30:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:30:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:26:03 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:26:03 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:26:03 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:26:03 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9024439080c5fee6414b5c4ed3fb67a4cba6098ea0797ba5845404b7a1d3`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 2.0 MB (1963367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63905ea5b150d55f3b79b38a5490837c24037c7abd8acd1d4162ee05f5a4e83a`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e343a2d6005f8b44b118ecd9d16bb3fb9be2c89363fec6739559a23202a55e`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de67dcc89abc325cda51ea490a783c6d19781f93c56373d1a93cf5382c124f`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686191425faec729397c7fbe27f40b57c8d3eb25035da6b50c85bab3f035a90c`  
		Last Modified: Tue, 19 May 2026 20:30:31 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8938cd886756583b3e2e8f621d2518666da25bb8a79ddb2882b181f90749810f`  
		Last Modified: Tue, 19 May 2026 20:30:31 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071e2b8e443aeb6dd786e344c945cf2caa6830b85ee98d5c665836738318644`  
		Last Modified: Tue, 19 May 2026 21:26:16 GMT  
		Size: 20.5 MB (20520283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:162b220cd47282c910ab8bfd8800200c13fc3eafabf76400c8c5dfa92e547839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.2 KB (903214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ad0e32798b48ffb40848dda3fef12967f072172c536d72ac51d6a0cd19d90f`

```dockerfile
```

-	Layers:
	-	`sha256:295df4a4fd7f2794fe07c25ba54688884a268a6c355d244a41f0b8acd2080ce2`  
		Last Modified: Tue, 19 May 2026 21:26:15 GMT  
		Size: 881.8 KB (881758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb751aca59442eb87cd3c674276a3999cd1471ecbcfebc75655d44d48a73570f`  
		Last Modified: Tue, 19 May 2026 21:26:15 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; riscv64

```console
$ docker pull nginx@sha256:6f2393fe55d6ada9f214ebf149e9fc9d7c632164e322f79d5af6962938292156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23505888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6456061658c5fb4051484107ecd56f172af239f67be58407f7682954f5eeafa9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 23:17:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 23:17:25 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 23:17:25 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 23:17:25 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 23:17:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:17:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 23:17:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:17:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:17:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:17:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:17:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:17:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:17:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:17:26 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 20 May 2026 11:58:11 GMT
ENV NJS_VERSION=0.9.9
# Wed, 20 May 2026 11:58:11 GMT
ENV NJS_RELEASE=1
# Wed, 20 May 2026 11:58:11 GMT
ENV ACME_VERSION=0.4.1
# Wed, 20 May 2026 11:58:11 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00efeeeb0246d365ded3c4a13699635cdcc6b390d7528c58b97f6ac5319c4b47`  
		Last Modified: Tue, 19 May 2026 23:17:51 GMT  
		Size: 1.9 MB (1917642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a625ce065afb99d4b04d66ff51d17b8dd435d9ca948426146520fabe5f3dff6`  
		Last Modified: Tue, 19 May 2026 23:17:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f0fd85b008b60aff425c69bb3be782580d7248c92a82fdf6bf642acdf5ad5`  
		Last Modified: Tue, 19 May 2026 23:17:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8090984156439f27170393a3d78e651aef742f508b180dcd1718a866b39e85`  
		Last Modified: Tue, 19 May 2026 23:17:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3d94245a787545fbb11d8eeb41187775c3205b480e53c63536f8ecf9f27d83`  
		Last Modified: Tue, 19 May 2026 23:17:52 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5749cb0f699d8709035053cf791490ab74fd5f1f24a0e2c348d2ffce191561`  
		Last Modified: Tue, 19 May 2026 23:17:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f84da6ada4fe670d956c4522ba91fe0bf093caba7023a62616ef3239a2499a6`  
		Last Modified: Wed, 20 May 2026 11:59:01 GMT  
		Size: 18.0 MB (17995981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:5baa564b451b800db7f8551706a7b3daa6376246ca8d65a488222a1d768c4a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.2 KB (903210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3662ffa647409998327ebd611d2e52f4a20a35e4eec2012a395b057776ef73`

```dockerfile
```

-	Layers:
	-	`sha256:8fdb752abbf02d6bb49e4205c5cfed9ee1d8370a2ce8cba8ce63a31285b81b94`  
		Last Modified: Wed, 20 May 2026 11:58:59 GMT  
		Size: 881.8 KB (881754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c28ab25eb3ee65bad5ea759402549374dbc29d5a36758e4700d9850bd3f15ee`  
		Last Modified: Wed, 20 May 2026 11:58:58 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; s390x

```console
$ docker pull nginx@sha256:91ea6de17f1045f3201e957bc74324e72ab86abe63b70528a1f57258cc3d2a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26094632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea31846e74b36cc49e1d28afd5b9c8b7f1e6da3bc0fe9c6a514cb9d067e5cf9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:16 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:14:16 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:16 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:17 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:20:31 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:20:31 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:20:31 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:20:31 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b718a481eb6a1e5f2702e58138ca2c5777099b6cc9261b3ee04793b43d6020f`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 2.0 MB (1989873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4018e9f1117d94f9914bcae655876ec203350c75c066f70bdad78edad676d4a8`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e419add5f5b4e45c14b8e385639597a6e0349f06fb065a0464bdfe68f0b80b4`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ff5d09575651be88dbf61d1dc5b6fb3938ba26cdda3be8c819813395fa87f`  
		Last Modified: Tue, 19 May 2026 20:14:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e839d4891e79770219b732c3961d69c0a218ba39a8da712870b91b933dafa7c`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343d5fa069debb586f160051765d31650ec33eaf57f468c92e62a60a6350803`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52566b1e9fdb4348ac60c7634f9a1ecda25b3b227a8e64350219c2646a8739b`  
		Last Modified: Tue, 19 May 2026 21:20:43 GMT  
		Size: 20.4 MB (20373634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:7e9bf2c8ea18cbbc44c75587d50afa19b8958c9e4bba1541b211fabc5bdc4cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.1 KB (903112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122fac51e057b2f6645aae48fbecfae9249f6c5735085c6a12ee3069ee2739ad`

```dockerfile
```

-	Layers:
	-	`sha256:11f5bb34214151db83839dae5c5e67b6b13d670c085d657a2afbd9eb5ca0ddaf`  
		Last Modified: Tue, 19 May 2026 21:20:42 GMT  
		Size: 881.7 KB (881712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947df84d6dafcccb42d978749a66731eb040d4545851ac52878d24d935026ccd`  
		Last Modified: Tue, 19 May 2026 21:20:42 GMT  
		Size: 21.4 KB (21400 bytes)  
		MIME: application/vnd.in-toto+json
