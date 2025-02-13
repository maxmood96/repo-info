## `nginx:alpine-slim`

```console
$ docker pull nginx@sha256:d7a882db5450b0f95c8ccf6797d9c4a0c14b9d34f4d4fd66289e6125b95e7989
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

### `nginx:alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:7271e2f985aadf78ea09c68452a101bac8e681e1779ede04d742929ce11b017a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6a84c112116d3fe016e60d0f1f400bd28f71b60a23f0e6b449f3a183e8a1ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5215a08fb124932f41461b5da64ff183d8772c8cfa6d2ba64447f60275113f1b`  
		Last Modified: Thu, 06 Feb 2025 02:16:15 GMT  
		Size: 1.8 MB (1789009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8813b38090d755304b9b62b790b0f19cd7eee409c3d0a3d495411be8eb35408`  
		Last Modified: Thu, 06 Feb 2025 02:16:08 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f41882e104d5e4b0e443fc387e440da00594e400a8c6c8d426e86a910e11084`  
		Last Modified: Thu, 06 Feb 2025 02:16:09 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92b9802c411990b7ff95ce238004213125726f1586227fe2665b765cd833602`  
		Last Modified: Thu, 06 Feb 2025 02:16:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b56e0e1b50da94d716fc880809f96d5cb2751e0d9d9c680ae6c60e0f9239708`  
		Last Modified: Thu, 06 Feb 2025 02:16:10 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5281c445f8b7ca564e8124519f166a63c67a38074755a2d72738be7800dbbc78`  
		Last Modified: Thu, 06 Feb 2025 02:16:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b951636cfaf04730aa532316064c08e78d2d269b65b6d2243e32914ba5a0995b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.8 KB (500834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeef586f80eec6406553fa729ae969643bf8aa594db70090d1e95862a97e245`

```dockerfile
```

-	Layers:
	-	`sha256:98269c88703ad263c1d9f1fe8a30209c4ddb0cb11ea191df6ee4546b27a40406`  
		Last Modified: Thu, 06 Feb 2025 04:20:11 GMT  
		Size: 470.1 KB (470062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81668eabba294fdbbc60486ca4a9c653db32f70e4cd76e2ced727fe9d247c8bb`  
		Last Modified: Thu, 06 Feb 2025 04:20:12 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:0176ed1ea6d2ddb1ed58e649f730617f2acf1f9167a5bc9c87cbcd3804b66a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102f82843a743a5fa07d6735fbd8b36421f50c8e16b191c3ca475b1482fc67a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8069242372a84606a654d9f863997e74e73c03132ac533ea1a4029f074ac4b`  
		Last Modified: Thu, 06 Feb 2025 04:00:21 GMT  
		Size: 1.8 MB (1783186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b064f453733d00a4414e0e48672e817f402f60d4f1dc71ab51a145a43ca5e6`  
		Last Modified: Thu, 06 Feb 2025 04:00:19 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef21057fa1a028277d3d43d7624be6596e5d35414299219caf8500dc8f275e`  
		Last Modified: Thu, 06 Feb 2025 04:00:22 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364eade215aa7673ea3738f66596be2184e9b1848ee578c6d8a7e19dcbc17d0c`  
		Last Modified: Thu, 06 Feb 2025 04:00:23 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75f46d194ab03283365c8567c638e804d9de6047214a40a33e922fe5b329243`  
		Last Modified: Thu, 06 Feb 2025 04:00:23 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5c70190498c064a12b04e18d533f7b90a6346333582dde99ee28237483ccf`  
		Last Modified: Thu, 06 Feb 2025 04:00:23 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:90a085423ccf987646247e756cfd19976e7259ea527a6630104ba3683fd9f7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41cd2cdb9a11ae94f672fcf09a42085ef0d26ea21af08b25869a2db59af4784`

```dockerfile
```

-	Layers:
	-	`sha256:6a8168703c2d29be9415c6d1f657357a23898181b9748c544003367dc7491c57`  
		Last Modified: Thu, 06 Feb 2025 04:20:18 GMT  
		Size: 30.7 KB (30681 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5d24b202ce0982a864a773b77b4a8c86c3746015126c99cb7166dbad32273893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b446e20977902b85a2fbcc540d04f1464d81b4895be73508626b0f0f4f9f62bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67dc0dd30204e2e90016f49ad85cb0c864e81a25741c34c68a609777b92ab7e`  
		Last Modified: Thu, 06 Feb 2025 04:00:07 GMT  
		Size: 1.6 MB (1619146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ecf0fb60a0c699a2769a2e0f9d95a3ddc19f21a350535edecda46297e1d9b`  
		Last Modified: Thu, 06 Feb 2025 04:00:06 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b962a15c5993651a631d578d1d4ef2a56e7725307b4a5ceda0483787bbfb6d8b`  
		Last Modified: Thu, 06 Feb 2025 04:00:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3043cc9507f9730a3888b7d000a266fccc076b1f29f44856330dbfaa9a62881`  
		Last Modified: Thu, 06 Feb 2025 04:00:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1611e2648ee8d5b5dba0d40636eff81911f9e8d2eb1ee55b5618895d2d71afc6`  
		Last Modified: Thu, 06 Feb 2025 04:00:09 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1abd9406cd6368d98073c395ce4a3eb430c4e2d0eba4ca30a80328d1a39b4f`  
		Last Modified: Thu, 06 Feb 2025 04:00:09 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:2806acdccf537cd5bbc270da3b39dad823372709dab133b7991eac8c0e7278a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.0 KB (501042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239f7547873f00831c9148cc07671c5681e5cfbd0486eceaf00cea8b97d99f43`

```dockerfile
```

-	Layers:
	-	`sha256:2c1cc0c363bed3f74ec8200aaef0c0e663c0add2ceaf9ce38fa3ac10203b06a4`  
		Last Modified: Thu, 06 Feb 2025 04:20:25 GMT  
		Size: 470.1 KB (470146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d2639e19483ca50b64e09b494f23c6923e42105521df76fd20f6e200bdf2cf`  
		Last Modified: Thu, 06 Feb 2025 04:20:26 GMT  
		Size: 30.9 KB (30896 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:43fdcf80420442532d01ff621c7a8dc514c17d9837c88996d0c8056f5f10ab2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ef244c450c466edb0841a9ceebb37ba95f433f27634a40425bc8f27d40efcf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7881d666ae1e7e1d2c967e53593819b6503e5d686dba95a109421cbfc51450da`  
		Last Modified: Thu, 06 Feb 2025 01:59:56 GMT  
		Size: 1.8 MB (1780468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f256ac5fd451ec18939846ff7ed223dd1765a9f82fda67245d30931b74b78c2a`  
		Last Modified: Thu, 06 Feb 2025 01:59:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967eb288a8baec4bc92d2b26d5bb3aae030792d2204023b8917218ff4c1db80`  
		Last Modified: Thu, 06 Feb 2025 01:59:55 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1232554cb43555bbe242a0624c2112090e184d8aaacced677bd08b6f97ae4a27`  
		Last Modified: Thu, 06 Feb 2025 01:59:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df7581e762b82e26bda5775a6b9836af9e5864099fb02f529ca40d0c8ec1cb`  
		Last Modified: Thu, 06 Feb 2025 01:59:56 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0422927a03f94f34f1a992ea153be7d24ca83113863ff4c7d17dd64c2e6f562b`  
		Last Modified: Thu, 06 Feb 2025 01:59:56 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fc8fb49541910a2d4fff3d7ef0996cbdc81fcba9699a15ce1feb9d8c988a6db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 KB (501138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc25cd0556e60867b09b894463e0e5c8a1838bfaba4dd8ef24d3379146ca4cb`

```dockerfile
```

-	Layers:
	-	`sha256:68f110bad5871922126c321124333e55633ed6f6d12669753cd50ca777ff5714`  
		Last Modified: Thu, 06 Feb 2025 04:20:32 GMT  
		Size: 470.2 KB (470190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd639b090fb01e3d455ad8b26e9e0ab973fc7376e952c141a9bb725bc22b5109`  
		Last Modified: Thu, 06 Feb 2025 04:20:33 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:51fbc88f8eb7fa70d2330bdb094d898b377b4f71494ff36abe3cb6da0c880d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16b752cb693699e64c3947bac732419ccf1dd62fa056455d025fb967322aea7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3856c088e2e9df6696a270267dfec2995727966c6fc3e1bb8030337d884936a`  
		Last Modified: Thu, 06 Feb 2025 04:00:42 GMT  
		Size: 1.9 MB (1857642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8813b38090d755304b9b62b790b0f19cd7eee409c3d0a3d495411be8eb35408`  
		Last Modified: Thu, 06 Feb 2025 02:16:08 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986328bf8882dce919f8299f77b5fd81571ca1dcab08af406426d79672770a5`  
		Last Modified: Thu, 06 Feb 2025 04:00:43 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8454111c4e5ea7fe6efd142e26c9fd033802d66a5a33c91bbc45d3fbcad2bef5`  
		Last Modified: Thu, 06 Feb 2025 04:00:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b6a7000683f322b29cbc999d038c1554eac83e2e88f31c9ad9be96af176ea2`  
		Last Modified: Thu, 06 Feb 2025 04:00:44 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e57a5511ec8811618fa28389c3c8cd54cff1c5f17d0f6988060d27f097f44`  
		Last Modified: Thu, 06 Feb 2025 04:00:45 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f60aec9255c1a67a95b68174d36ab09d36fa1435db1bd8e99f45cfc65f3926d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.7 KB (500717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44ae6a571f8cb94bd315f23f861e4a8671987fd9cf11b903a1688a6dd2e5b1d`

```dockerfile
```

-	Layers:
	-	`sha256:bde2c0b2d353c5f69ffdabcac5fab95b2dff4aeffc0c0837b8da7f64c36d8fc2`  
		Last Modified: Thu, 06 Feb 2025 04:20:39 GMT  
		Size: 470.0 KB (470007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76fd3aeeb01c331ac9402348b03dcefb0e4b0486eee7fc81daddb3d45b3964d`  
		Last Modified: Thu, 06 Feb 2025 04:20:40 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:357be350015136d298385dba921abe0c563e0cab3ab69ff93fb7766b5adcef07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4879225591346bdd79bda694697350c39e44b1f3024ba51d735a6c864dc32ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e51b1b46b70cf2e9ed5612649c7ec3c119d72e5909cbb4bc1cceed1d657d29`  
		Last Modified: Thu, 06 Feb 2025 04:00:49 GMT  
		Size: 1.9 MB (1852728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60696ab7b87d1f69b4dc3640e461fbb02170677a54d6fb9b0f01f03759ab20f`  
		Last Modified: Thu, 06 Feb 2025 04:00:48 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f13d1cb01835ef217413f7d050b3ecad2097255ec853cda67d35621cc788e3`  
		Last Modified: Thu, 06 Feb 2025 04:00:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a8a8cf3956db74c5e3465ce0b0eae66fc2f3bc4aa2fc18e9abd5a80cff177`  
		Last Modified: Thu, 06 Feb 2025 04:00:48 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa115446a5d1bd369a66673dbd6e8e5d16deceda360c2307b25fadac7131e6b`  
		Last Modified: Thu, 06 Feb 2025 04:00:48 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449e5920f33c851f7f61e29707fb37d9a8e5eee6619f4d4bcf5931125e802e61`  
		Last Modified: Thu, 06 Feb 2025 04:00:48 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:281f7fbb72e2c79c12f2de673f1d44ad0ab926ad5e4a617af59721a60af91c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 KB (499032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518c7d7fb015cfe814038b3aa73634775475987eb3c3b807e5c98db8c3c495a4`

```dockerfile
```

-	Layers:
	-	`sha256:29ac434801820f3b96410a72920a2633d3cffc79e37d34c6fdd8408e42c0ce39`  
		Last Modified: Thu, 06 Feb 2025 04:20:47 GMT  
		Size: 468.2 KB (468181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c639517686671c99c4bbeebd0a2617907ddbae155177c50bd71a7fb1f756ca`  
		Last Modified: Thu, 06 Feb 2025 04:20:48 GMT  
		Size: 30.9 KB (30851 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:7a28d86c0d593f57cd87c68e4d5c8b01eb69ec15d46a5fd40f22922c80d2c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5180442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0513854ec9cd56355a7ca2dc80216aa8dcefa4a6c7ef11c9bfa4a004aee46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ef55168e3ac2d697c2c523b5bfabb26a14ce47a0d012148b634a15f80602f9`  
		Last Modified: Thu, 06 Feb 2025 04:20:50 GMT  
		Size: 1.8 MB (1825584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d5d73b7034d4721faac699fa0850313159ed421c12ce3adfb490b59fb497b9`  
		Last Modified: Thu, 06 Feb 2025 04:20:51 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83303f92bba5b3020d83d22d29e73caefc15a90ea7167273134b83aee31c212e`  
		Last Modified: Thu, 06 Feb 2025 04:20:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035cce110326f8a2901a526bdac8232ee657e77857a366930128cf38ed57856f`  
		Last Modified: Thu, 06 Feb 2025 04:20:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe964c2e37e2f269c70f905738f113fe9a4cdc7fa94e91ffd7eb9b29a0453ca`  
		Last Modified: Thu, 06 Feb 2025 04:20:53 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18590b5c35722ad0e1136d3c04c043f4e488d0912abd3b8e4e04e9423a7ad8b`  
		Last Modified: Thu, 06 Feb 2025 04:20:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b2189b91acff7dba79272386e228eb6607bb74e00b3d8a01c71805a7e7d3b6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 KB (499029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b8246f42e8c0a19b9fd6b496b26918000148d2e6ca394991e6deb9b71dce8`

```dockerfile
```

-	Layers:
	-	`sha256:4e44842c3c25e74039325047ac2c15df1162097101e70fde4f088ca10c0781ff`  
		Last Modified: Thu, 06 Feb 2025 04:20:56 GMT  
		Size: 468.2 KB (468177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1163e2e7c1339db38b66a083cc2539c450a0558602ec56d1d90092e502631488`  
		Last Modified: Thu, 06 Feb 2025 04:20:57 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:ed47529ac7884ce43a0a806f6c5bbb329025ffab37eb142f46038902e8aa5eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5358549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9048f90d343821093323a338d4b96f1340fd758f986be3206cc3e643eb29cdbf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cac9d17a141c007d1a7a5ba85399751f66214628b402e3cc002843bb4d798e`  
		Last Modified: Thu, 06 Feb 2025 04:00:51 GMT  
		Size: 1.9 MB (1887084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb002550b2bf12e0154879990acbb8bed3fd5bd2aecf3cf100c9aa81c10a22c`  
		Last Modified: Thu, 06 Feb 2025 04:00:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d43579712b13751b29c34d647aed4b5d591bb7905b09305f583e6bf6b99b737`  
		Last Modified: Thu, 06 Feb 2025 04:00:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c7c84054a608aaf1020a581999db0e314a3121c8d70c1b4aa1785cf515b718`  
		Last Modified: Thu, 06 Feb 2025 04:00:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca50d4e59c9856f6f0f89147e13c70eb37f0a806bd3b6f3910a828a46e13805`  
		Last Modified: Thu, 06 Feb 2025 04:00:49 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25474e2d9922512e476e8a1735741d4721bd45ac47d7fb9c8205a1a0fb6bb4da`  
		Last Modified: Thu, 06 Feb 2025 04:00:50 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:dd58f5c40d15e2aa165510ef9641eea33e41c9e0e05fef62cc1725bdbb56b714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff02e587c28147343caf955e6ea6d7e7d5446a811a95d2b61e9da4d3f6df6ad8`

```dockerfile
```

-	Layers:
	-	`sha256:ca12eb63db8bd8fda9e6982a3848c6a44dfe63927924665df3b65a29447d25b0`  
		Last Modified: Thu, 06 Feb 2025 04:21:04 GMT  
		Size: 468.1 KB (468111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71eb5f7fdcffc0fd0689f978a6c72a1a188b4ea23b4d94a8f881f6c0daea26bc`  
		Last Modified: Thu, 06 Feb 2025 04:21:05 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json
