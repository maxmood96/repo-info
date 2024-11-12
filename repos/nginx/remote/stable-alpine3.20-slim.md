## `nginx:stable-alpine3.20-slim`

```console
$ docker pull nginx@sha256:7f7e572e2201ac983620ff8312436e6f4a061bffe097b927482f1b490031097a
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

### `nginx:stable-alpine3.20-slim` - linux; amd64

```console
$ docker pull nginx@sha256:cd3eca87df1a03418ee28a1c139c3720d8f51a1c5f1ba893ce8d8699fc28af82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04818d62b638d1b65ea9d8df70cf9648668784ef89c6e35e00b04a07e4422bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a30f47e80f68c8b080b9caf937bee7938f9803e28ace93fa653d99bfec79c8`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 1.8 MB (1753596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64d3291c88487893c3e040c5d6267ca61a293c54953b6c1d2ab737a6cd4bc2`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc0279166b1d5f2003017604f19da153fd3d8d206fde5db1e99c904fb5c9a86`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b17590914c3ff6bb86b151d2e6138fb098b4a0353c28b9be0070c223a02998`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d6cfdb81c676070f0c829560da6a3ac61bf76f70948e1cbd8f3b62fd011703`  
		Last Modified: Fri, 06 Sep 2024 23:21:58 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6592d833752c39e0409c309ed8d8596fa19fc8f0f4239d326a1cad81a9b77b20`  
		Last Modified: Fri, 06 Sep 2024 23:21:58 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3f2136e548432b4fa7c12d29efc7c5880d6526ad17017e9aeabb95306c9c2aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.0 KB (493040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e813882737dd7f804a2c029573faa8cc88ce21740097f31b7f661f2e3098651e`

```dockerfile
```

-	Layers:
	-	`sha256:c362940f3f2a90b7d3858803444ce7f14539170d3ffd7d2df06ebfe55f11a35b`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 463.8 KB (463786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb0c1bd1cadd4c663dc70fda94efcd617fa605ea830d19a7e9fc3b71763325e`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 29.3 KB (29254 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v6

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

### `nginx:stable-alpine3.20-slim` - unknown; unknown

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

### `nginx:stable-alpine3.20-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:0fba7b6a13565f3a155b59321b8b5a2c93f2f32b47a55ce72b53cfae064de94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4824431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066bab52dd6ec570d47bcfd6fbe71d78d8f4485f20b81dad9468189c46b34e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5d3e352e3985e7a0f14409a8ed0049b05e2899b93ca9109a3f5c277351353906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 KB (493179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb3ff33b3ca2ff67c2996f55c73d6d4a3ce12c83cebe92cfd0f2d5d01700807`

```dockerfile
```

-	Layers:
	-	`sha256:fc1dc9f62d195685460ebd3708f92c033dd99016913cb89329d66c00ed6f7660`  
		Last Modified: Sat, 07 Sep 2024 03:02:31 GMT  
		Size: 463.8 KB (463838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de7e338cc85cf5dd51bb88be0806730b7b684db67eac92ca33810420d13dada`  
		Last Modified: Sat, 07 Sep 2024 03:02:30 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a86436d9467da0af862d0ce6b5887946a0028291daa33a2f14918a20d71b46e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c972149fbca733e70719c0e8c8551f56fb795b7789ad287f12976714bfdc37ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:18dedf31cc44ae562c8ea5c741e204c1a6386b2d36745723b02569c566b383f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa3bc620322c50ff2d711f8af9af8e4b895d0a6e208a720299e5776a6477e`

```dockerfile
```

-	Layers:
	-	`sha256:3d448e6885a661cd41c78c5d547a1c6b398109a54f376f0f4f0dec95ff975f10`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 463.9 KB (463866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc913cbbea26b3f2af1ddabea9c8ca4858b24f5c1789c35936f59fe7718abb1`  
		Last Modified: Sat, 07 Sep 2024 05:31:51 GMT  
		Size: 29.6 KB (29579 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; 386

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

### `nginx:stable-alpine3.20-slim` - unknown; unknown

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
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 463.9 KB (463857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f957b3684d63f816d1a5b99a38c17f5bb501de4a4d96048e3d7b2f262ecaafb1`  
		Last Modified: Tue, 12 Nov 2024 02:04:53 GMT  
		Size: 29.4 KB (29428 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:aaa8c70eaf475ef65d779f05e8d6f8a13d6b3cdc9021f7ec83b9be9014adde35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5524104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e137584c00ca130f7e3b89bc914c86cb5d08630fd12403f4bf37b281efb08eef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce7041ab6f5aa0b01bd714e8b52143b047dd27baa61e9112ad108690c37d01`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 1.9 MB (1947095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a389c5657440b5a4de5d2e09ff26c071db81eaf84f09e11b0b974bf0aedc708`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357293aaa474a46824bd0db6a53ebcc410447a3da42fb326101d51c40086ed90`  
		Last Modified: Sat, 07 Sep 2024 07:08:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c243b6b33077d582edb46a6c6e6c581756eb7bcb7c91ea4cc9cff77fafadb4fd`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093624ec0c439cd3f27dbfbf338723356c50a5ac8aa2fa0f13727bd434e1b3a`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f90de16503d0a74d573549cc8c6653ae41a60caea93664db5907af8149cc339`  
		Last Modified: Sat, 07 Sep 2024 07:08:02 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:677daf54d3dfb3de4c9f06e3f7654373152a3d80b3c86d91af05cd61ee208d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 KB (491183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734ac07551084f675a5e5d1e004b2f4de9942ef9eb2bbf9718d4a061b414e4d9`

```dockerfile
```

-	Layers:
	-	`sha256:cd74b2cbf68498d70a543c3e93afb263a878e848dba3f393db26aebf901d640d`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 461.9 KB (461878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd5905cd1d8a2700b9bb52ac58cc7f3fa95e6fdfff9c4c8440107fe3e9c428e`  
		Last Modified: Sat, 07 Sep 2024 07:08:01 GMT  
		Size: 29.3 KB (29305 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; s390x

```console
$ docker pull nginx@sha256:bc0524b304408def8d1bcbce1441256217e4c456147abf6ea6195da7c760d96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd251a43e028bfe7b0afbad5ab5c680e967ac20aa99a85d3bdec666140d799c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:942b7d8b1ed9211455ff511ace67264f9071144ea983fbc52e34904d08b2142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.1 KB (491085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eec9d90fd722c5760f9ca143d676bcbbf4121f355b61da9401a7e666281f834`

```dockerfile
```

-	Layers:
	-	`sha256:5363e477a1b2f427707536cbc8146ffe3f214463cdca10bf9f9f379e1f051182`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 461.8 KB (461832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c84ec8b95784c03e630255145e2105416526074ce49ca612a1bffb80b082c5`  
		Last Modified: Sat, 07 Sep 2024 02:54:29 GMT  
		Size: 29.3 KB (29253 bytes)  
		MIME: application/vnd.in-toto+json
