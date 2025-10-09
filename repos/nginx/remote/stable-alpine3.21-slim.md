## `nginx:stable-alpine3.21-slim`

```console
$ docker pull nginx@sha256:06b305b18588d92b4b5558403146c1437ed778ca31349254e77c4feccee6a0b3
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

### `nginx:stable-alpine3.21-slim` - linux; amd64

```console
$ docker pull nginx@sha256:eb8c00e3f75d52947cbfe3cc352671e70bcb78f850be8b64e6bf9652ee8853de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5438579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c83a2a01fe2ae843fc2bdd4c9bb73064f58215f93a226445a1e443806c4f3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8554c5f1ad0265d1dc3a5f23b3b52e93fa1cdeda0c6b54618d3f9168e6ed01b`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 1.8 MB (1791417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e049f0fd1511eaabb03da73d0582501fd3a012ddb00620ff653b1a13b646310`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a39d0d04b2893246ec57f9cf1b074a63fd0f094098a8b1741d0e625f4009c1`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6918dcfd20da0647335265f4647268123ce772646f9dea11cae650f26be0276`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fca37af7b3b885e76d1a14e76d630444c2868b27ff67848e077142d9771faa`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d7488b05ed88bc5975378fd4ef0f1ea4b6114d13fa5cbeec6a572588e0c00`  
		Last Modified: Wed, 08 Oct 2025 22:40:03 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:bdc2866e44d6a27e2c46bfaac77ed8e23fa7801198c66d4cfe16535aadb62458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.9 KB (500885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f87893a74f42ae2d5edfe6ab0a1dfc82adfa360e29b5eac54cf6b9b9e51dc3`

```dockerfile
```

-	Layers:
	-	`sha256:f22928bc0042f2325bc19fa0aa67ef8d7b213f1fd894ecaab44a94fbcccfc09d`  
		Last Modified: Wed, 08 Oct 2025 23:52:17 GMT  
		Size: 473.3 KB (473258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aafd690cf262fd69e57973a1817f23d42272618a3e39ef87bc638d0c080cc4fa`  
		Last Modified: Wed, 08 Oct 2025 23:52:18 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:10dab83ea27d582607580848af6ab443274377c13a3d47ac6f97a16c2816d959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5158246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc2bb735dc8aa68bfe81ea4520c43b3573e7ad39100a441e31665dffd8a17d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07682950d586b292ace9f6b133f2117e18311c17f184b506d4d771e9e1f6383`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 1.8 MB (1788188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e358ed169aa7a5072ff8175c7f546e3758f37663f3d5bbef6890796293b327`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74adb3ec51eb38f527c2a4cc7aea3ce5afc7c4adcf83f75d11f3a895eb74d01b`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e34c6d03ca54ee2c91bd2743e881e417818414c57ec5110e735ca4d8ee7859`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd546c1fc1bc2a9d443afe370b17bc4d52ceea5e36a13663e1094984a5a7db84`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470f6c431369fd5ed80fd5d249ed199d654f599978c4e86ab225190e72f8763`  
		Last Modified: Wed, 08 Oct 2025 21:43:20 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6ec1ef767b45bad86e2ca8b34c20255a63fb6ba5007dbefe89067bc5db0a729c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfdd51dec25b8d819faf2877a449faee8acd573802b05558035fc8e7c8d2aa0`

```dockerfile
```

-	Layers:
	-	`sha256:12b395bc302e8e0ab0b960106d2c3d717c5f635e460119056ee24e75c447786d`  
		Last Modified: Wed, 08 Oct 2025 23:52:21 GMT  
		Size: 27.5 KB (27507 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:52a4b8be6b68f85775166aeb6cfddfd6198a1221ab4562a6c09bdfc801e4c6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4726484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8283fba958a75c477f77c1981ff0707afc0a402ec82a83e036ab3e5244b8c186`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6db0312581d04e55ca347f61740b3986abb23d7533753516afdf85111455076`  
		Last Modified: Wed, 08 Oct 2025 21:44:07 GMT  
		Size: 1.6 MB (1623272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf0f6822ae6cd4a22754dafde63614d4ce41520d97f87ea554f1f9cfd469e52`  
		Last Modified: Wed, 08 Oct 2025 21:44:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3bf35aa3d902abd0867da1641426094423d4d81ddbdcda5146561fbeb7b07d`  
		Last Modified: Wed, 08 Oct 2025 21:44:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093d38cc75f77dac8baf2dbb30d39129de871b73d13519ec01bbc51825ea39f3`  
		Last Modified: Wed, 08 Oct 2025 21:44:06 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13d4f308be343ee7b4a774d4ed1bf3d183bf14ae8509df6a28665306f811d7`  
		Last Modified: Wed, 08 Oct 2025 21:44:05 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1386217021219c463948ee93cc2b3aa6663b636bb8499c4101a16b5820e70`  
		Last Modified: Wed, 08 Oct 2025 21:44:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6ee30ca4311cca694ee3070738c19a034b7ca8ffa66cfac66067c12fa23646ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.0 KB (501033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9017e0995ab682e7b4bc4f6dae1ec9bfa0ba885e095382327c9a11da187c7c81`

```dockerfile
```

-	Layers:
	-	`sha256:8635e3935595f11125b215870d89d41ad63c0e64fc4dc793a114b51a382f7712`  
		Last Modified: Wed, 08 Oct 2025 23:52:25 GMT  
		Size: 473.3 KB (473310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f9b7b7f9745a5f76f9522fdd06094d37cf16015c1f30bf9377c8a6013d2c6a`  
		Last Modified: Wed, 08 Oct 2025 23:52:26 GMT  
		Size: 27.7 KB (27723 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:cf0f6a2acd16fd75e9dd7fcc571fdcdf1acf1c29fee0194b240ef1faf30e1b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b09f3e06eeb359fdb00899f4d90ae768f84d85ae8305d798d9ba72579ee9657`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad5ac8f8cf55b8c0c82be0a300d298fc22b9758efa86180f462ceb53853d8e6`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 1.8 MB (1785854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71a558a48478f790729c9b8c77049b95f6b818e252ad6e71c922bfb0d9bf7a1`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75955c831fea904d11c6a5975dbd4d0ca0181eb9c9908186675b0cf99fdffca`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0758cbe9d05315581dd3d4bd237636a2dba151678766235eb71805aa1c7eea4`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a330f762070768538bd31e1956316de88caf4d87a6148749a5482bcb1442d63`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf803132b551abfc9140e3ae8b047edb8f19216239e131cd96352844a0667a3`  
		Last Modified: Wed, 08 Oct 2025 21:29:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e5ec4653c82e065e7a87e2bf285047e19b368c769325dd07ceb19611ade8f213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 KB (501093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4699ac2f5f5e6950278cab173d763c1941f7ac4334dcba8ba9f31fd4b55a5db9`

```dockerfile
```

-	Layers:
	-	`sha256:cb14eee6aed5d900e038a078fc62c0d1a0a4dba8af780b83f09a914f49295b18`  
		Last Modified: Wed, 08 Oct 2025 23:52:29 GMT  
		Size: 473.3 KB (473338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:221c6db90cc369d56b595088072feedc21654915ca6c41e2530bc7b4c7e36d0b`  
		Last Modified: Wed, 08 Oct 2025 23:52:30 GMT  
		Size: 27.8 KB (27755 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; 386

```console
$ docker pull nginx@sha256:2b3a4cd6c8e63db04dac348cced3d12973c384fe13af965652a62e73ba1fad3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc47c18ddc85fc43cf8ea78ad95e70680b21e0d38d6ff62a19966b18dea15987`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e16b5198bf3cb91e693a106ae8f6b74e4fe6d325f90b181a2d97e06f63653f`  
		Last Modified: Wed, 08 Oct 2025 21:26:05 GMT  
		Size: 1.9 MB (1861100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf6bdbda03822fe46dae183aa1a2420ecca6b4a75f473141423be2085a37ff`  
		Last Modified: Wed, 08 Oct 2025 21:26:06 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b779f6a9e236cc4c50690a1d61d5f68c9ea8dd7e509cdf7b5d3dce39d28dbef0`  
		Last Modified: Wed, 08 Oct 2025 21:26:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7bd12b77af3b62863c3fbb2f088b915eade484bde7253fda9b276b828a2763`  
		Last Modified: Wed, 08 Oct 2025 21:26:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0279d1138d0fd53a17398981493360a087dcc9deb6c3227239863b97ad2a77`  
		Last Modified: Wed, 08 Oct 2025 21:26:06 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54149fec425ce4ab40a559a255faaa72917960cf67e030b6429b03da69bc1a38`  
		Last Modified: Wed, 08 Oct 2025 21:26:06 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7db172dc2dd3e3f7ee4aa96994f9cde647ab346bb466a359889e5f48ac54888c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.8 KB (500808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb41ffeedde1b9e731762b34fd3841e61e7e6ecc0b3fa2035d3da0461473c308`

```dockerfile
```

-	Layers:
	-	`sha256:5b5a8eb81d0278ab2eaea272320925d86dd475cc4ee28120bf40db266117d4e9`  
		Last Modified: Wed, 08 Oct 2025 23:52:28 GMT  
		Size: 473.2 KB (473223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d580d6a354724f21c2aee40aa79e88c1f96493fb8ccbecf2f64da8771b47bc9b`  
		Last Modified: Wed, 08 Oct 2025 23:52:29 GMT  
		Size: 27.6 KB (27585 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:81fb20d80d4f14811dc3bb05968c026a8249498ab500393c934c8fac413d13e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626c0446c8db23e5463963dc24c4c75b8848b85e0fc427e9b2c1ac519146c48`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 13 Aug 2025 16:03:17 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b295ad6b71e1a4e2631cdc8b8a85069a822292a9270a0c518d14657855269`  
		Last Modified: Thu, 09 Oct 2025 00:51:38 GMT  
		Size: 1.9 MB (1856782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba09b29355a8687d117885dd8bb870050fca89d8e6207f20dbe98a5bda2a5b`  
		Last Modified: Thu, 09 Oct 2025 00:51:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03300db9a2e19ece2a0787c51f92e3ab53b4bfb3c7078b51704af6a234f3e5fd`  
		Last Modified: Thu, 09 Oct 2025 00:51:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1507e8b5d45199c28b32c893fbf4f436a7011c94235868db4d1f110d0b47b1dc`  
		Last Modified: Thu, 09 Oct 2025 00:51:38 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b868b2bc8bb1ab5053de5fc1fd0338a36510a36296fd51e009c44479b4dc03`  
		Last Modified: Thu, 09 Oct 2025 00:51:38 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75225864c235c002e3d63848b40941b9dafdc56396817bcb084018f5742a4ab3`  
		Last Modified: Thu, 09 Oct 2025 00:51:39 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:4fee55cff51d37c417c8c08079c7b6d4c35b144e4c494fbe5aaac57333cf2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 KB (499036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7cebe4988453053b66d7295cf9b0a0eb4eb294a983ea5955ca0702a938fc45`

```dockerfile
```

-	Layers:
	-	`sha256:a1ce83ab35c667f4712a310c8ee8968eb41073b16d9587e2a8e3127c1df23665`  
		Last Modified: Thu, 09 Oct 2025 02:51:51 GMT  
		Size: 471.4 KB (471353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a4d46a46c3682febcc46f2b1745d46ff243dcf429e313100634ee4e76f6c9d`  
		Last Modified: Thu, 09 Oct 2025 02:51:52 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:fbe362ae06a86ce570d176140453610c10f4a0d7ddda62ccc17b3f0168a65536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5183950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bae0b57f3a622f431d4c356cf923f385e0cfc16b20419e5ab455f64c2d5adaa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dea8ce60f1a295e561662edd4d59a28e4e43d5e23ab71c192dc7ae61a5ab54b`  
		Last Modified: Wed, 16 Jul 2025 02:39:41 GMT  
		Size: 1.8 MB (1830268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944c13e5ea9bac45420a84a250c4593771a1bd589d1aeef23162d23ce838613`  
		Last Modified: Wed, 16 Jul 2025 02:39:41 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8097b1ef55db5b6aa24c15d608f79d03ebb4281cf47ca0acdcdabf7d18b16258`  
		Last Modified: Fri, 15 Aug 2025 10:20:02 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b2545dcb8576851dd5e1543a2de2dde769b14cba3340b62e73dbd3c5bb9144`  
		Last Modified: Fri, 15 Aug 2025 10:20:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee8b45c4c97fff1cb05cd019b0ad50823c5671f7287747800ae64dbdc04bbe1`  
		Last Modified: Fri, 15 Aug 2025 10:20:02 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64001e9db0534320a4e5f63817ff151256828c54ce9f8b01d8ef56bd1b80786`  
		Last Modified: Fri, 15 Aug 2025 10:20:02 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:668191f695d4dcdf739cb60b0ab978220ca2e03f530e05bfdd4c77432dc89a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 KB (499032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7862422725ac60999db593bd8db904cd9605e98c60464d8163fbd149eee172`

```dockerfile
```

-	Layers:
	-	`sha256:6628103a8119316892b294375026eea540a738fee1467a9df3088a40bb2d164f`  
		Last Modified: Fri, 15 Aug 2025 11:50:58 GMT  
		Size: 471.3 KB (471349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c4ececca02c93cf27957f2dae364e4b8d4188761a9236b1070676308d7f2a6`  
		Last Modified: Fri, 15 Aug 2025 11:50:59 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; s390x

```console
$ docker pull nginx@sha256:216a6e7259c17d6700884be52d46492fb4fefa263991eb567ab3984c76322110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5359024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50367552aa033369f00f47dd6cac8462ee29d786ae774e0f4776474700550cad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:03:17 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 13 Aug 2025 16:03:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:03:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:03:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:03:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:03:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:03:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cf0ef344786af9e4ae7f0a97402c5089d6cd26ff884b4abeac9aecd8e90977`  
		Last Modified: Thu, 14 Aug 2025 03:10:28 GMT  
		Size: 1.9 MB (1892326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4b26f88d69ad96435cf66c791a289507eb252ea26d84f53865c5ea2ed82a02`  
		Last Modified: Thu, 14 Aug 2025 03:10:28 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eda5f6d24b2f346729079d45e66cef6fd4e22973c279bf2cdf9721c38d6fd1`  
		Last Modified: Thu, 14 Aug 2025 03:10:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec80d55db706832ed783ef0a322ea1f75e82b5d79a1d61de90d1da5fa5534f4`  
		Last Modified: Thu, 14 Aug 2025 03:10:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0a9fc4473e2602bbead26c4ce98b0f43ca2cf85b66f5cee17ca29fbea25285`  
		Last Modified: Thu, 14 Aug 2025 03:10:30 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dfaba65a57a4e5a93eb65471a15d871e486e7c19047f76ff1965c653bd975e`  
		Last Modified: Thu, 14 Aug 2025 03:10:30 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9e8f5061d30a04f31f2b0fbdb906362fe0b4223e86f5e8df8ae2feafb1300c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8a01d72e94486158ef5094106dc8aeae795e50f07836fa3bbba5360cf851bd`

```dockerfile
```

-	Layers:
	-	`sha256:9b78c2b7191f776683a17524bba2cb54942610d1435defbfc4a2ed98443e5dfb`  
		Last Modified: Thu, 14 Aug 2025 05:51:40 GMT  
		Size: 471.3 KB (471307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d511db87b8e331cd7230bfe5a61fc2a93664bdb30d3fb6913d5bf65cf442bf3`  
		Last Modified: Thu, 14 Aug 2025 05:51:41 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json
