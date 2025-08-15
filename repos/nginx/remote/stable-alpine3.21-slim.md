## `nginx:stable-alpine3.21-slim`

```console
$ docker pull nginx@sha256:f25f852134140e003ac967604cd1f9004a5e6abd195e8bf59bf0de303c9df35e
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
$ docker pull nginx@sha256:f011b028d9ab9032e7bf61de849713021d2fa18493b87bfcb3a9331687600133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5433584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ac47bed05b1a212e9cfbca5a4d92643ade29ad1995ba399c4875a709268f04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669998b1fdf4ad752e6d1b278e90c3634ca699b0394fc3fe7342e72d404223d1`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 1.8 MB (1791419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95be0f4718a48e45cacbaf6e19f7aed48101465aca88a577bd84a57ee42eba1b`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c31b33012d33aa0a2fe15793525a9d6d6bf9c57f1f9ec22b88a02f869b1c3e`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a0985bea3a96919f3334aeec7cec165a06ffc948c8de0418026c0d516c7016`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8485f215491f7b3eccbb9a4c66ebb932c076fa9d17aa985155b6c57e132c2042`  
		Last Modified: Wed, 13 Aug 2025 18:52:30 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0d37ae31d4ab6192eeea9aaf8c1c83664db1db36cb22c98fd2fd259c1542c`  
		Last Modified: Wed, 13 Aug 2025 18:52:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3d1374e87c48f3dde5c0cb4a614a079cb4a373d7ed22e2077c9b2d5183c74410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.9 KB (500885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab28b4e8c1c13ecd25de9488d41b3f4f147f8142ee55904ae46f5746875196a0`

```dockerfile
```

-	Layers:
	-	`sha256:0d1417e1befc9872b90e4de4ba4bbb83c6167c4d383234be1897047653af3e3f`  
		Last Modified: Wed, 13 Aug 2025 20:52:25 GMT  
		Size: 473.3 KB (473258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351302d984da2b6570236422eaf7beb9b21732299e8c9b2459bfcde9cf24dfc3`  
		Last Modified: Wed, 13 Aug 2025 20:52:26 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:89182cfa146e5b228507dc9990c7c1e83b5046e1e1efeb24e91b56c3cf3a491c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5156623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fddf95e736b2da60080843b4fadf3bdb56052ec1ed3f824d59c7adea611cd3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
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
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf3e13e92b3fc16e71ce7a4e0971829e9b9d3c5ba5ddd5741629c555ac53f70`  
		Last Modified: Wed, 16 Jul 2025 06:35:13 GMT  
		Size: 1.8 MB (1788218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfda9d17e0889232338e636c65b92aa90ea0d1cf5835e7d11ded33f714d2dde`  
		Last Modified: Wed, 16 Jul 2025 06:35:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8838f88ee189507436c70047e225513525e4dfe793abb605699b717e2c267fa`  
		Last Modified: Wed, 13 Aug 2025 18:59:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05635194b4863f3f01279ef0e8ac9752aeed1517c8f0337ecfd2ef45abc147f4`  
		Last Modified: Wed, 13 Aug 2025 18:59:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f731a9c07736b42f55f388dfc88faec058e540d9bc0b394180a8941d5672d658`  
		Last Modified: Wed, 13 Aug 2025 18:59:38 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aecbde7a70de7f54f83908eb68c0b24e0ab6115cef000f711f4353460da7a0c`  
		Last Modified: Wed, 13 Aug 2025 18:59:42 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c6686bb95b64372aaf7cde7e9d50c6c4c80672a6f984c22d3322b14a30d3e84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4f3ea5417b7caaba15a2eaaaeb32cc0b3f795e861404d4856816d004a82056`

```dockerfile
```

-	Layers:
	-	`sha256:815765ec2e9c0bda71da7566c4960741fb2ed904c01711d968695d99783ba217`  
		Last Modified: Wed, 13 Aug 2025 20:52:29 GMT  
		Size: 27.5 KB (27504 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:88bb144bcd303ab6be570acfdd2a250ba84d6ae0be793bc6862a667b50bff283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4724732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc1643baa0ac915e68e2437ddda03bc89053efb9b8cf17334f4106baa287fa6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
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
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8a593d81c4c1f3c0c3d0fe072ba7b3c9f59c6a896f290e4b6872ca9dde86f`  
		Last Modified: Thu, 14 Aug 2025 03:37:42 GMT  
		Size: 1.6 MB (1623265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49121da6d77a1ced62cfbe13850b17b23bb6dbeebe015d6b1ef2dc0a80aa0546`  
		Last Modified: Thu, 14 Aug 2025 03:37:41 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a877592d616defc580376a8a5688cb441f6d2e37f2cbf3d24da5901db037279`  
		Last Modified: Thu, 14 Aug 2025 03:37:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d7d294755c68e3edc00b1dc81fdbbaa6471f91f709570e534de14583f9e124`  
		Last Modified: Thu, 14 Aug 2025 03:37:43 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1363cc15ff9b6d934c54c16bceb6e7ce9ecc728b70c56bfb15c74a531494421a`  
		Last Modified: Thu, 14 Aug 2025 03:37:43 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c61af6513562d5205b02e1e2b56b1199076aaf7bfe530a1c8e4772f88fb7356`  
		Last Modified: Thu, 14 Aug 2025 03:37:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:045f56202d4685bdce23aa384baf8bdf87afa6a6d2bd8b5266e76cab5d810b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.0 KB (501029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf38da9f5dba2becf53f995e9e78eaa4fab653bb949a95f302776a30e10dadd`

```dockerfile
```

-	Layers:
	-	`sha256:bc14f48ab1d03fb5f9bf902ab5a41589c184e3cea70b56b10acd3dc9428ffd9f`  
		Last Modified: Thu, 14 Aug 2025 05:51:28 GMT  
		Size: 473.3 KB (473310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1d65561f5f43da1c269bfe6d47f914e21419bdc0129b1bbb34f334bbbbaf88`  
		Last Modified: Thu, 14 Aug 2025 05:51:29 GMT  
		Size: 27.7 KB (27719 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:3b71e8e42ab52a043708190343949a3332d4e5bc7134b0545cb07eef0c980bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99aa10e5c232eb558759c9c75e3347febc2a7de97fbaa974b97dcb25c8fee7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7a34873ed7d54ffaa0e6b4355819114ccb01229e8467607f6460a7d87586e0`  
		Last Modified: Wed, 13 Aug 2025 20:43:48 GMT  
		Size: 1.8 MB (1785856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6a496a738990b686922a1d7a2de9015eca5b3612f06f78c4d155e499a265c0`  
		Last Modified: Wed, 13 Aug 2025 20:43:48 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d1fe6cbe22cd85690516446836d9394762eedb2ec6a0aebc16b903c434385`  
		Last Modified: Wed, 13 Aug 2025 20:43:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dbac7ab7341163036286e0c15f482bfa9471ef67b18fc571499d4919b32e34`  
		Last Modified: Wed, 13 Aug 2025 20:43:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a55bb04d0604790d28e47bb200077a985768953d39ffa8ed20e25b7dd9343`  
		Last Modified: Wed, 13 Aug 2025 20:43:49 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4841cb53dc6eec5b48197fec8faa3838e9f16a9cf16ace09e539aa20b3caf09`  
		Last Modified: Wed, 13 Aug 2025 20:43:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:12eb27f394391f5fe92f6ad6d8def0615e99fee7ed979235f23f94ca7a4cf676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 KB (501093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a39a3b25b3d33ded1bde8889da89d432161c148d9bfd65b67486796e3a7b1`

```dockerfile
```

-	Layers:
	-	`sha256:deca632216b0434f77be42fa28d2db6a17489de5146aa61d47eed8566882a56b`  
		Last Modified: Wed, 13 Aug 2025 23:51:44 GMT  
		Size: 473.3 KB (473338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b6603425df9dfc691a4436640968f2f654107766be766753a6509bdcab0921`  
		Last Modified: Wed, 13 Aug 2025 23:51:45 GMT  
		Size: 27.8 KB (27755 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; 386

```console
$ docker pull nginx@sha256:256d0acf1de9d0de3cf101772d77cf036bc69422a307969385b8494ef33e7b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4e4ee600e081b0d0a302160029d9e73b9d14d02d6a641f8a0c9215cf9f664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
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
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61695b11a1c35c3a5845c08fd77c539f59226141fa39c6e213c6311aaf9956a`  
		Last Modified: Wed, 13 Aug 2025 18:54:07 GMT  
		Size: 1.9 MB (1861095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4bc88118958e19233341d402ad72aedd2c43f1bb6b15adf585133651ce9cef`  
		Last Modified: Wed, 13 Aug 2025 18:54:07 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bbe7cbe769d3e460d68f5bb4803576659a04befdad0db17a7f82386fe6693`  
		Last Modified: Wed, 13 Aug 2025 18:54:07 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81de44238fbeda3be1c183978aa596ad455e5fc1ce0e64cf76ffd24c55ee889`  
		Last Modified: Wed, 13 Aug 2025 18:54:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5944a6938d4304f10fe4b6088e56483a12edd7af5424bd1479a2a74a893e36`  
		Last Modified: Wed, 13 Aug 2025 18:54:08 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39917d20a1ca57a498b8e9bdd3ba8d24992303c5eb5fc4a31134b872a01c86`  
		Last Modified: Wed, 13 Aug 2025 18:54:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fbe5928a16f76c72e68d4f0cc0735de8fd7039676cf7b2f8e9392246c318a44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.8 KB (500808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a314e2ddb9e74b939ac971f961d7b0c50bec9e65e00b4ec7ea2a7714cfb4a96b`

```dockerfile
```

-	Layers:
	-	`sha256:9e7a8896668ae0371d9aa8d816681512008f62dd5c1c001133ca3974d3cebc8d`  
		Last Modified: Wed, 13 Aug 2025 20:52:36 GMT  
		Size: 473.2 KB (473223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ce624092b2a2e6d4abdad0e931c747d6274320fe0a36377244c1e636cc2738`  
		Last Modified: Wed, 13 Aug 2025 20:52:37 GMT  
		Size: 27.6 KB (27585 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:cb2515946caeb7efbd3e9c949ce0659ea223b66e701fe91c200837f21a6c6729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414af4edbb480717ead0eb0756c501bb93e1d786e33b3896a1cea2d6abe3e025`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d43d1291310d5d9610165df537b13c9276f95ee211cfd93396a6189438739`  
		Last Modified: Wed, 13 Aug 2025 21:40:21 GMT  
		Size: 1.9 MB (1856799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8272ed6d634701a7f5240cfcc4c0990c05b2c488a6115cce2b71d0993f3ac7f`  
		Last Modified: Wed, 13 Aug 2025 21:40:19 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e20641a690c474a294af4010dfa476dd67cffc4cefc949d007190c4a1cc871`  
		Last Modified: Wed, 13 Aug 2025 21:40:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42f58692bfe0f912816f2b5e9bda1b38a3dbf86803a8e6293effb2d5527ada`  
		Last Modified: Wed, 13 Aug 2025 21:40:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bcd9f4417677c5aa189df1c3f66918df9102433ea4c21b765fd90c2e3211e3`  
		Last Modified: Wed, 13 Aug 2025 21:40:21 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467f71fc8eddfd0e435d293281d12f4a0d494ee231a9287d3a7fbd81cbd64236`  
		Last Modified: Wed, 13 Aug 2025 21:40:20 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:ee92ea8efce0275825a65ba16492b89129685057efb7ca015ba829392dab51d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 KB (499036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0421a7ae26d2ea5c86e0be432f165c2f3b0ee6d65376815a9918988bc81633`

```dockerfile
```

-	Layers:
	-	`sha256:664f9c7955e967b563b8f12bf6bd31012020e255e2966827bbbe9529d4a259fa`  
		Last Modified: Wed, 13 Aug 2025 23:51:51 GMT  
		Size: 471.4 KB (471353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4bb8ff1aa06a65cf5e9d861f2d583e25b214d9f5869b4d41b75e226ff5341b`  
		Last Modified: Wed, 13 Aug 2025 23:51:52 GMT  
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
