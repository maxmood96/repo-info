## `nginx:stable-alpine-slim`

```console
$ docker pull nginx@sha256:c13d84b525bee78b8761523bf5ab1985b86a4aa6682a226c09c55eb875373cb0
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

### `nginx:stable-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:c843d4684c6aeb8663e4716b7063941370fdd9c94f452cc0fc55d7bc8105f64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7662441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec54db690b515c7cf751f989d74b66564f2613cec906a55ca28833e39b2c2a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
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

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e20a7acbadab33aaf3dd2b04ce909e445320385f5b94164afea7d4b5045fc0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fddd0e07d77d789a344fd4f809d6587a621d208b3e3cedb57c1e2bcfd3b7c0`

```dockerfile
```

-	Layers:
	-	`sha256:916013a13c4f140c7f67d7ea182d5b2d798d6a9987d7903513e8fcecde8d1b56`  
		Last Modified: Tue, 12 Nov 2024 02:03:16 GMT  
		Size: 463.9 KB (463892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e215effdda9b717b4f605c17fbc4c4e3d62d5b77d702d05610e402c3a4163e31`  
		Last Modified: Tue, 12 Nov 2024 02:03:16 GMT  
		Size: 29.5 KB (29470 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:ef9da845de7d04fcadaf69863955b529ca220d61092850582cceb5a09d8cddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1613221fb0fd4863222beda6a44425ff152282e0be456168e7bf884d9f19629`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
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

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c668e0547e32663f59322e8364c4a936dea776cb7e4329be613bccc4a171b04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 KB (29346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb823d5e065518478ea2325c172ca5233b1615973ca1472a0f2243b7c20050ae`

```dockerfile
```

-	Layers:
	-	`sha256:265d54a0cfce989814003e0c00a81bee9a4df9b77cb647b76557f57951fcc7b9`  
		Last Modified: Tue, 12 Nov 2024 02:46:45 GMT  
		Size: 29.3 KB (29346 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:12b40836ae2ef8029928cac89e8da00b7e3116f3dceec185527a339f63b22eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6621737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48693a20319d05caccae5f2ab0418ed351e3aa3a0b0d3a1f9ba5348c814f9de1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8312fc93e5f4a7405a6a40b2841f7e792a6bd3e76dc2feb6441b8188cca25`  
		Last Modified: Tue, 12 Nov 2024 03:04:03 GMT  
		Size: 3.5 MB (3521661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6f287315adea558d39a61b70d823d6fac51717499cd31bf8bef67a42f0e062`  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10baf2b8799849cb17dbdd4d38850d2c24065576742ee6219ecd7e72a2e1278e`  
		Last Modified: Tue, 12 Nov 2024 03:04:03 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909f8693fd11d6aedcaa6c068cdb3f508257bfbae63762a4ddec22a2ed939f10`  
		Last Modified: Tue, 12 Nov 2024 03:04:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3f0f731f3044633478967f61abb8473fb94324d83da90c657067d8bd8cf76e`  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b044890f46b5fbb94afb3d37f0c4356d625b47ee9fbcbb66e318ffc30e87adc3`  
		Last Modified: Tue, 12 Nov 2024 03:04:04 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3969f8c343b2ad6c60514344a1a8c553b8425139d88c6e32705822c66b008a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.5 KB (493506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72fb512a9bb7bcdf71a9f1441accb48711a35e4b2f866fb54481613043b117`

```dockerfile
```

-	Layers:
	-	`sha256:c9fb86a803f28456e3659244e7ad74825d91545e154c6638d6fb5535ea971e8f`  
		Last Modified: Tue, 12 Nov 2024 03:04:03 GMT  
		Size: 463.9 KB (463944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf5891689845f4b41ea0cdfbbc113aecb77a807e3707d7eb88faf5e1939e572c`  
		Last Modified: Tue, 12 Nov 2024 03:04:03 GMT  
		Size: 29.6 KB (29562 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7147ff96c4ac80c37c362a86324d50b22c1b9b80c40d191203efac9bcd79f38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8574290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76b6cdabe8497359092e734a8b3db90757a849be1523bbc9c7c297317baa67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55de6ab04a8543673e0e8c608e1b6174e2e14896dadf4c77a8310260f117f9a`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 4.5 MB (4481980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0827d28a368dd6c3ada1bce054af2c1301b74fffedbd2dc2f4fcc03d577b97cc`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f277b11af5a10c20bf2bbce7393f04ff0caba77088cbabd4b589a9c1fa860c`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee80c16a5ca2cb359dfd85430032a1377e2ae91ba4eb5299f0336de1c1f863b0`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce55efd2df5a70d0328787d87f2cfa3bbbba592a88b2881a3e1a1978532d228`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34138022de30a9b98a5cfd6b0dd3528979572f00a1a0ffc561c9ff6ce1491ce`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:03d7918b09ba10a67bcc4ac1f4548f1d8d7eb76e674da1727a3746b301debd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.6 KB (493570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5de012ffd24b5958a051717991066a6ff9b0728ddd20ae35deb9e85dd0a3078`

```dockerfile
```

-	Layers:
	-	`sha256:84d39f9ac871b48795576f9b6ccfb7a5e2233cb2aa31a7b9f5b315ccc394b29e`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 464.0 KB (463972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3adc8d5061e91f948ed0dbaaa5fda180c9f4c969b275d452f3134a863e35770`  
		Last Modified: Tue, 12 Nov 2024 03:28:22 GMT  
		Size: 29.6 KB (29598 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:55263101218a6b0e322a304238c5332ae3c27a5770a5ed000bf961d9b154658b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f6e9b1b72fd1bfad1316d7a2be100daa41ae5753d44102b7ec52a1768ce31e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
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

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:222eacbda55a864e81ee04f85dec8c0d8c5b53b4e3a5c719b575abac57d13156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 KB (493285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa851487401f784f73483a456f4d8d6fff3c571dfc35f43e773b445c30561980`

```dockerfile
```

-	Layers:
	-	`sha256:6808582f5449e534a1fc89b3342aafa34f6b3fe2c7c8a68d54c473f0001de10b`  
		Size: 463.9 KB (463857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f957b3684d63f816d1a5b99a38c17f5bb501de4a4d96048e3d7b2f262ecaafb1`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 29.4 KB (29428 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:5255befa132f2b5c904dc328d302224ae36d3379390d76517a0ece1b0506532d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7671994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09dba56b3a25db4005b30b2bf5237f2acfaa70506f5aa2a2cc2e861362e0b88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
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

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:2b52107fb0e3acdd1dacbcec334826f8da12e9e4d95c4ab41451da06d5af4a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 KB (491506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98535e74d10aca6e0d8241ee2894a05a93432aea1f2ff7966bb75fe407cd6dbc`

```dockerfile
```

-	Layers:
	-	`sha256:a7cd1d0f59c977732d739085b74a6f4c7bf9a32d2e8fa98874523c868ff473ca`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 462.0 KB (461984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2e9d8c2e92b3432df970965437fccabb3250c499c2a6528dd0e149d9cde63e`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 29.5 KB (29522 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:83ec95db20d8960b8c4b966ec29c34075ea3b7de0d449d0d1dec16fab9dca4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7263885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e8b4817cfc933bb6cb3612434f39544469f2f1ca175658bc20d3c51a6ec11a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad6cbd7ff44fcf04946245bb3601f8efe5acd4026aa225855f027cc9789ebe7`  
		Last Modified: Tue, 03 Dec 2024 02:34:12 GMT  
		Size: 3.9 MB (3887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0cbbfc15b11c7be123874c52730c3cf3c6e3bd42664614c95f900378916908`  
		Last Modified: Tue, 03 Dec 2024 02:34:11 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddddf734659136063407b009d3ce26e9a076d409c139fd1005c28a962cbca5cb`  
		Last Modified: Tue, 03 Dec 2024 02:34:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f846e604ae7ec5a6b11eccb945079566c455001d311415be926e4acb2669f4`  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ae90c7ffaa4a4342fc79ed6595d845eb0dad059df854c9ca2fe4e9441a847`  
		Last Modified: Tue, 03 Dec 2024 02:34:12 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3ca6f36c6d3f8475c14e5facb812d2fe17f415370c09500cfdf61858a7452b`  
		Last Modified: Tue, 03 Dec 2024 02:34:12 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e4895fdc3a756c09ffcaa212e4a25a10a2c49bd78250c4e0af8abb87b74cc0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 KB (491506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1458d4a9ddfea958565c1d83e7ac1d4af479b897288ad7e98b5903652209ef1d`

```dockerfile
```

-	Layers:
	-	`sha256:db5594d113a65651a423c2932041d55e1f5f2bccbe3292d3c6cc4abb01a79664`  
		Last Modified: Tue, 03 Dec 2024 02:34:11 GMT  
		Size: 462.0 KB (461980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81df723e12028bbd38bd8c012a0dac978595beba14637a9dd66677e0c5cb10e0`  
		Last Modified: Tue, 03 Dec 2024 02:34:11 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:c4060340f4c866bbb76d57882eb08076f8f36d809afeec206b187c893a3e48f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78fd3e2093f640492548d649aa5b812954bde995e0b4cdb7552a759b47da73a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a72b82e26db69bf0df3a32d34cd1775a16fa6604ed1e09eb95566da49c76ec`  
		Size: 4.0 MB (4014361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9a5684fc8098d31d84ca46770025844865c82ba7159fa40fd635217dbe54ce`  
		Last Modified: Tue, 12 Nov 2024 03:09:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70246586be2b4326bd73f9aeef2ab4b75bf23a89d40f8350c6039cc09e1ac738`  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6431873c315a4752dab8925e67d6238a271444a114d1a176b76ba00b61aa6bc3`  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c264419ea5b57ee947db607d246dbfb6e9b2f65f30fa3fb5c2b5372aa42785`  
		Last Modified: Tue, 12 Nov 2024 03:09:31 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd344599ada0b2da804d7a8fae22294e4993caaccbd57c562447aae4438ca62`  
		Last Modified: Tue, 12 Nov 2024 03:09:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b397eb2e896bc3567b371aecddf5d568cda338e07e4f71df154be210b3357e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 KB (491408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4988211e8b41188d65c937cd7b2263a8d9ac54b360817fffcfd49c8a0dfdcb`

```dockerfile
```

-	Layers:
	-	`sha256:56d12b35201e98def0b38438679909af54d143e49620b4d8f4e12ea2841f8a3c`  
		Last Modified: Tue, 12 Nov 2024 03:09:31 GMT  
		Size: 461.9 KB (461938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18458bcff2041bb710ca92ee5a4776b20cb88eb7c20fe5e1d738c24fc2052b07`  
		Last Modified: Tue, 12 Nov 2024 03:09:31 GMT  
		Size: 29.5 KB (29470 bytes)  
		MIME: application/vnd.in-toto+json
