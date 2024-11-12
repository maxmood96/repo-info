## `nginx:stable-alpine`

```console
$ docker pull nginx@sha256:07c237ac5f9834477f46ed53f3037298d150307ceed0eee851c5625d5ce2ed56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `nginx:stable-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:0c454cfe6ed8a8aaa83cd55901c193890a681e5340b62cc4d0e6c34641cd11db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20871556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60847f99ea697d723c3c98e70276c5ba8f6072dfd5fc3202bf4399d27cf7883e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b4536fb82bbca5d4c7493bf7d136c22659364305316d3f9ca32c5e4e33968`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 4.0 MB (4033949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9301b75a59e749446d939ceea4bd5c30eb8d3ab8be72db8ff34e55b02b0cf937`  
		Last Modified: Tue, 12 Nov 2024 02:03:16 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e73dd210e16faaadfa5bbd79a360d8f49b9131927fcdc7a03ed473e7265f6`  
		Last Modified: Tue, 12 Nov 2024 02:03:16 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715a1066dac6b2b7cd4e27b179a47e1024302cbcdbfdedd99a4053caf7dae55`  
		Last Modified: Tue, 12 Nov 2024 02:03:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19f1e837fdf987a6ac3a4758cd73009ffeb0e22e3fa3f477f2bd6fc075de241`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede6cd11b30508d9e2d029a3d2c4c164aa86f2c8f6cb10cc1465bf7623a5161f`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e76302afc66c622dcbb0c717f47cfa38fcabfe05e5c38c1436bf84f7cef1f5`  
		Last Modified: Tue, 12 Nov 2024 03:05:28 GMT  
		Size: 13.2 MB (13209115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:4abe114b38b993c78cbf777f6bac850cf744bea126f404ae9bf260edc1bb28a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.4 KB (884410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0310d0e1c46c699c1f8dc98cf69b2159c357795ba89cffe88660b7f36b201e36`

```dockerfile
```

-	Layers:
	-	`sha256:84d8aac288b6eba255499f394ba1eb821c2644d9419480465734c11e01584424`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 864.5 KB (864513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20af4b3c81d20fe1f8f6d145f7b75ac9a3e9559571d702363202fcad599b0b6`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:424ad094b554675d2ee781893b2da9ce03c58d14f9ca555328e080ef7b4d5303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18387320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a80f28f76854e6bcc83f83ae16da2945ef2fecc12f715572de468fcb9c36ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9037a3e6b406659e3c619df09fbde1eb6b5d6d140af832d4be48c2c9a6b1ae1d`  
		Last Modified: Tue, 12 Nov 2024 02:46:46 GMT  
		Size: 3.8 MB (3838017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d08a8fb5b930ed79f99ab39fb90cde1bf023a9d4c9d9d14eaefab52380fc9a`  
		Last Modified: Tue, 12 Nov 2024 02:46:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68366cd6088a72532c911181d0a16028f36529381aedddd681d81109881ae416`  
		Last Modified: Tue, 12 Nov 2024 02:46:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b454f080f91ba2cda4791c36512a5ffe9b3fd148caba43ec8befd002c3ce676`  
		Last Modified: Tue, 12 Nov 2024 02:46:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa9f5e6741dda8107d5784a23b279d561620a929b5f1c2ab705a7c872eb58a1`  
		Last Modified: Tue, 12 Nov 2024 02:46:46 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9810f5ee6827751d83dc7060681e238cd0b53a5f841dc06d3ff1e02dc17cac`  
		Last Modified: Tue, 12 Nov 2024 02:46:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bf71e88f14f7b78b598b10b206976e92c3f917cbbe1bb3d10bca4a3337c144`  
		Last Modified: Tue, 12 Nov 2024 15:46:57 GMT  
		Size: 11.2 MB (11178121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:a0a00c3e47adeb4e55ad5a8fe5cde415ad5fd2bf1e6f57b6a6edeaac83d06dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab960539939996bbab268531002a49cfead58925e3b2bbb6a1823fe3c6a3cb`

```dockerfile
```

-	Layers:
	-	`sha256:623a1d6766e0c54d37900709dbebe93f6d04f3445020ff8c939e7e3dc4f0aefb`  
		Last Modified: Tue, 12 Nov 2024 15:46:56 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:4b1575e04d7953fce66f918c8113df66eaf69b68e15977e4a15cc06356583b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16550971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4467d1dedeea97e3c7f9d37ccbbebfe533f752137bad802cd3edb031bef55fc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc18c167cae876e55129d1d2262e9d9b54118aa4874ff4299c71b8ada079c06`  
		Last Modified: Sat, 07 Sep 2024 03:02:31 GMT  
		Size: 1.7 MB (1724338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1000656e8457d16a38d59199759396095e590acd5a3fd747c52a7f53a3931a3`  
		Last Modified: Sat, 07 Sep 2024 03:02:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a321762a2d15c2c39217e6533fadfe3d7fa693a7abaeb3cc239f36858b2cac`  
		Last Modified: Sat, 07 Sep 2024 03:02:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0255e944350798d35bb0fbc4de0eb15a496d236af1ddcb8802f207cb88e1335d`  
		Last Modified: Sat, 07 Sep 2024 03:02:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5da8645f9b54c4dd116f8657c4530498ad5dcd2d9b6cfe43ab2a3087d1b2`  
		Last Modified: Sat, 07 Sep 2024 03:02:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf02d151e5984d1f3962178fc98297349a13fdc1f567fee07963bc32ba0c315`  
		Last Modified: Sat, 07 Sep 2024 03:02:32 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a1956b572268cf2fde0532c83faee8555e667b88d46c9aad191ce7bcfb9285`  
		Last Modified: Sat, 07 Sep 2024 13:30:48 GMT  
		Size: 11.7 MB (11726540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:e8c007d1ab9971053158d537ab4f03844dc42701aa6e531b889b949368470043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.3 KB (887285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcde3b47008b176f3033caca2739c353a8edf91b08de7e235b36ef0286b1534`

```dockerfile
```

-	Layers:
	-	`sha256:e499a88667fdfdda8d221c75c57220b1815c08890a7a56f33cd4d5df5c33e8b5`  
		Last Modified: Sat, 07 Sep 2024 13:30:47 GMT  
		Size: 867.3 KB (867318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61269f4847af4fe59d511f4306c78546749ee06534b20ebc99838cfaf6e6d9a8`  
		Last Modified: Sat, 07 Sep 2024 13:30:47 GMT  
		Size: 20.0 KB (19967 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:e935addddc3f7df1dd73c075c2c75cd4134f66613c5ac5df4267dbaa4238c057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19598794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f01cb019378e4f3da179880d52af1c8ef6d1103129c2a8aa1718ebd3ff3402`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acad845eeead560277678da1e4406d074bdc8a121cef597601d00a8f842f858`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 1.8 MB (1786717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0ce3a013e4d723b1853d3a3b7b162dbe77f5df2e733dea8841f31a7b950385`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9fd8d1267b0799ef0644949f89435e6038bf3c60a923b0d697415ff742e596`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f109e9a0d31dd3480d69e80ed2f1ffc0251bffbbbd704f7625f6b2c4205d24`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a996b223bf7c6657c38ef3a52691418101779babf6454e633074d6b52f11e848`  
		Last Modified: Sat, 07 Sep 2024 05:31:52 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea55393a485e52ad64a49d1567e6a1543c39a4ccf476361999ab3cd26e53b49`  
		Last Modified: Sat, 07 Sep 2024 05:31:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca96592c0ccf02939ac848910e5435444bedffbc69da445532c2ada9e9f04191`  
		Last Modified: Sat, 07 Sep 2024 12:36:39 GMT  
		Size: 13.7 MB (13719838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:4f09b310e8110e1d747cacaf902e5251dee1d4dd1ae25746c6303385e462e3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.8 KB (884767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9a5fa789249bd33d1f95dc1ddd56df0b9bc9437ff95384477fd9aaacc21bfe`

```dockerfile
```

-	Layers:
	-	`sha256:78f07111d548aa8684a93218a54ea682abe18e56c958d45eaddc4ea597fc2e46`  
		Last Modified: Sat, 07 Sep 2024 12:36:38 GMT  
		Size: 864.5 KB (864482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62ddc2600dc35614ed4d78718fd653692e799c180b075c17e51e65ea7f660ca`  
		Last Modified: Sat, 07 Sep 2024 12:36:38 GMT  
		Size: 20.3 KB (20285 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; 386

```console
$ docker pull nginx@sha256:d4e7f4c4ba7538c848e1c06caaaeeb59929a4e5bf4991c791ef7b981b8497ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19770423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30289849133e980deaa47630cfbcaf39302bb257ed6d48a95b8ad258dd265605`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ff8917abf32a129b7dab094dec1feb1033c899e9573f5161a636fc281dc0f5`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 4.1 MB (4074359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bfe83ae117f5a3d259f14247761152d0beaaead374be43941fcdce82dccc7`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3ac72ccb62774908725815f31afa16f874fa1c7f89233cdeecedc5250a265d`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4528dd79c36d470118bcbce4ff80f19a211228799f20c6f250b4eb8c7cd329`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c64b2895f1bc2c474168afde043856a9954dda464fc7a495f6227dba5d9396`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b49b6d59c4db88a46d891ec6491feb670f8bffd978f1b9be2cf8be20bbb3c`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1762f6fc7b62a6384e4d8429236eb6699620d0c6282640c015b28bda8fbcc69`  
		Last Modified: Tue, 12 Nov 2024 03:08:18 GMT  
		Size: 12.2 MB (12222261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:899436b7c6c33e768e2941c4c2729980594d9afd5b1e103207d672491b99d22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.3 KB (884334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6d469bfdd223643b09ba5d5d6816377d03bda7c22a7ebc84b3548c410509b`

```dockerfile
```

-	Layers:
	-	`sha256:ab1e5cec4afbabb7df8750346d08842f5a167b68451090679f76316ad567cc24`  
		Last Modified: Tue, 12 Nov 2024 03:08:18 GMT  
		Size: 864.5 KB (864478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34938b3f220c51437e018d6b048775c1658f970c04f13dd900f8eaf21073e209`  
		Last Modified: Tue, 12 Nov 2024 03:08:17 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:5ab8b38182b79e72376ccdf6a38a0d294d9c891bf0f69cf1f65ea438d18291ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21038255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b3c53725f98f83c2c7349929ed61ad5f0bc29545518fe725134ccc8b07e047`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32cf8448deac3a97be80b72303beb0da25f6c2d4a3f1d892acd0ed535898474`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 4.1 MB (4094948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daaa5b148c84243e780aacc26498d56ba6c576bcb0914c26b68602ddd19124a`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9b4850645839ac1e1c2b367023297f98877e8d560193e39512f28c93994a40`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f15c78cb30c74f33015766d046ed6e292a392b7ff589948ed67c0faf81c948`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e479b20cb8ed598869748a3e82fe8425eabd47e609e13465965219579f03126`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9109165d0307393c58fb71b394f93c97a59661152c996464b9d95622e6a807`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6390314aac73f6f40b31f2014640375835a036bf1a93bfac2aa9ab0b6c05a886`  
		Last Modified: Tue, 12 Nov 2024 15:12:30 GMT  
		Size: 13.4 MB (13366261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:2001ea99b448192cc21fc660035d4107362ec8a3ad73ceaa91cb2890c3fa6db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **882.6 KB (882558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5998c9ff21afc6ddb5aa82aefe6c3a44921d0fe4416f012132b3ad69bdef21e8`

```dockerfile
```

-	Layers:
	-	`sha256:d336dde0ec8383bd08fc534083fc2cb7690710cc71b8de2be73e8eae923e049d`  
		Last Modified: Tue, 12 Nov 2024 15:12:29 GMT  
		Size: 862.6 KB (862605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e88dce5c49057d6c422f544d25034e012aa3d0b1e1ec290bd272ea3c5e275b`  
		Last Modified: Tue, 12 Nov 2024 15:12:29 GMT  
		Size: 20.0 KB (19953 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:b945a5965c62e50cb0c2beb604ca9911b86fee5642cf1289fc0698d02cfeb380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19053392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd07355c28cdea4b0281335ee1d1072ca1c99562995c599cfc15790c99bba4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NJS_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2f8b174fe256a19d5af685d09f292eac9f42009f44e6d66b924b061d12cec`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 2.0 MB (1978717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682a9011d49ba0f89e6cf3d52240d0f07f51461c56da1c257d7cf2b020b73eb3`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3210ae0165a814db03509e49942b584e30f79ea5b60ccaaafa1f42f534075b`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9ed094fab1fb19e238dd9401b7f42fc358d8c82758c9aa83000a7be3e3fc2`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5830bbc8ce0e3ff6b492929e6502a4724d53994c50b86fe28e8bd0b8b2110`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c6cafb6e4127df43614ae345dc7e96d9beea984c1b565c45006ec7b80460b`  
		Last Modified: Sat, 07 Sep 2024 02:54:30 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c7a0c5ee69247bec776eb11ac425afd6c22298861d1bfd7e0a019b4671d76c`  
		Last Modified: Sat, 07 Sep 2024 11:13:14 GMT  
		Size: 13.6 MB (13608491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:8bf7b7d28436066d59bd015f36e0614e6a7270432c9e25eb4bb913b5d7e29be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **882.3 KB (882324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa1838f7e478c62ce09b80a6200f79c643e79d92048e64144dfdad5a3911a6a`

```dockerfile
```

-	Layers:
	-	`sha256:f947180e21197a2ba138fc62d200b8d5a702b1c0d42859b18889357e5a319dc0`  
		Last Modified: Sat, 07 Sep 2024 11:13:14 GMT  
		Size: 862.4 KB (862448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa61f86ec3822133a9d033438fb853050957b1d20f3e9111c3660d618a40567c`  
		Last Modified: Sat, 07 Sep 2024 11:13:14 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.in-toto+json
