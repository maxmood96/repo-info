## `nginx:mainline-alpine-slim`

```console
$ docker pull nginx@sha256:fe63f6eed1d853ccfd285870037cf1eb27b58dab767616f8f490df6e37f64a18
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

### `nginx:mainline-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:f3948ff2806a04de42190809a6921a131319b9c5ed3efead5c8671c94ec15b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb96e3e9a520d633e37afd1734d0ea4c619d8fb0756d5407db6d1302e9fee77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:05:55 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:05:55 GMT
ENV NGINX_VERSION=1.31.0
# Wed, 13 May 2026 19:05:55 GMT
ENV PKG_RELEASE=1
# Wed, 13 May 2026 19:05:55 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 May 2026 19:05:55 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:05:56 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:56 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:56 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:56 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:05:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:05:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:05:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffc65fde23e8f068ec0f227311955885730aa6251e6261eda658796680ce17`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 1.9 MB (1882811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eda4087d069b85f6fb7334775b687fd3c43e57e2aa5d5d88589666c6f4b144`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f24ddde8a46b34bf2ef16be01ea0701f6b281fd8a2017a95d44dbfa92110b5`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5351d87f1f6698b5b518ff527dd7a690d3f70d8a03ea902956a1c698ee90f6`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ed557e90381f9206a08d8362ab04dd8c15e09d644e5e2620793f67c684b726`  
		Last Modified: Wed, 13 May 2026 19:06:02 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19af4ef65048c9c32172d38f29283882a69ed174d3741ee3e0d2f65cc52d3174`  
		Last Modified: Wed, 13 May 2026 19:06:02 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0b8a8ca2bcd5c571f9cc1da371cbbb24ecf55709690c7917a2fdb5cad76c7cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 KB (505605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67e87a5a8b34a9300673564f05f0cdd85de1be0656df03ef6ab2481f67eb063`

```dockerfile
```

-	Layers:
	-	`sha256:e7eef4091832a61c28aefa871196b0c609c052a6b8354270110c47294524271f`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 474.0 KB (474012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee120ae7ea11725a52e3de027267bd9291b939740801bd1cc788dd1fc10d2d8`  
		Last Modified: Wed, 13 May 2026 19:06:01 GMT  
		Size: 31.6 KB (31593 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:5b8fb0a32b7e5e487c0127136cdbe42c4d9a2ecfeb222c36911e19b9f1b15347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddbc82c7c5265c0e8481f39993842a5d17d66f0a3c44226562d6f17c91cf166`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:05:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:05:17 GMT
ENV NGINX_VERSION=1.31.0
# Wed, 13 May 2026 19:05:17 GMT
ENV PKG_RELEASE=1
# Wed, 13 May 2026 19:05:17 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 May 2026 19:05:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:05:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:05:17 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:05:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:05:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3045be1c9a09aa4d82eafe6e383e55394ccdf2df1526dfc808cd20aa4d92697b`  
		Last Modified: Wed, 13 May 2026 19:05:21 GMT  
		Size: 1.9 MB (1883310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f474ba235a514e1109c0f80561550e775dd10465282f64f1f174d94ee576958`  
		Last Modified: Wed, 13 May 2026 19:05:21 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7866649b46a9e06a543a16266d157734107d9c4335444364b417ee76a75d4c`  
		Last Modified: Wed, 13 May 2026 19:05:21 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8184520caea6bd1f8948051a4dce7eb9c8db0ae7ad5b6ba6ed947567945ef353`  
		Last Modified: Wed, 13 May 2026 19:05:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9f45cfdf89d1c83772e2bf2387045ece83bef07f68820e9813453f5475528b`  
		Last Modified: Wed, 13 May 2026 19:05:22 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1f2a09725eac5d218708197dfd4d49b12a851fa22fbe1b6373d81c58ffd1f3`  
		Last Modified: Wed, 13 May 2026 19:05:22 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0d538b9ff0696d4ab79a8c71bf0bc49d3b8f3176c34c12a0d34443ab748f0cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609d41ddf79ea72005db5ce6c99075666c4ff31ecf347a848473bcae25907c4e`

```dockerfile
```

-	Layers:
	-	`sha256:c8e1443ae95a1a43c97dcb66224282274fa9b98159d89c0579e5ad96f6e31278`  
		Last Modified: Wed, 13 May 2026 19:05:21 GMT  
		Size: 31.5 KB (31506 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:4b53b96cde701b0a81914110408e54d38784b2f922c7c90a89032b8a5932f57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bf935eabcde34d93981c37a1023e728e699c8e4403db54ebbd25d150328c8c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:18:51 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 15 Apr 2026 20:18:51 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:18:51 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:18:51 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:18:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:18:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:18:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:18:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6056d71615dcd49d95fa883ea9a7eb510d7e92ea629d4a725359216df4cff4f1`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 1.7 MB (1693858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce8db47a86116460a68c117275456ab26bd30e2a3020e0c627743d1410a674`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ced64138dd6a728545d302ceef8f80188ade5e8f427d171918ad44b1120a0`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c027ca91454829d8b78a1e082d35a8c15bce413f2e2c6ef4141e8ee2ef0dd802`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b51e224823fad97a9570ba08f3f457254d6245d7f0d36a4521b75135eb7e166`  
		Last Modified: Wed, 15 Apr 2026 20:18:57 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85514863aef339136f2eb3b3870e397162efe87cc1d93793db1cee9d343f9f36`  
		Last Modified: Wed, 15 Apr 2026 20:18:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c631b5ee6f75f6298dfd701ad1b89f895630847fcaf7e90b6285c557de5201ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 KB (505167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4413eda03fea441f6f7ac9e50305715c0826226b2aa1c3330cce324cd6f4457f`

```dockerfile
```

-	Layers:
	-	`sha256:62c02e342a973541ea3d9fc5abb3122fa431ba2b9586c4b2e86a9fc8268fc4aa`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 473.4 KB (473446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77eec9b01445738ee2277458b2d60ed5c966673e1ca7ea373532792002635e7`  
		Last Modified: Wed, 15 Apr 2026 20:18:56 GMT  
		Size: 31.7 KB (31721 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:87b7a2033154a02a1e63ab3b01afbca39d54c006fafe265e19b45440db966da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6105706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ecea0b36282af904b9c48f8b181909ad4099e5ec0ee41ff680f4c39b73f20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:04:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:04:57 GMT
ENV NGINX_VERSION=1.31.0
# Wed, 13 May 2026 19:04:57 GMT
ENV PKG_RELEASE=1
# Wed, 13 May 2026 19:04:57 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 May 2026 19:04:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:04:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:04:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:04:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:04:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0ad73973d35ca8c59967827dd2b842414dc59f5903b871bb9f1a400453f2ce`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 1.9 MB (1901246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c893f715c738163e106a7769c15c8634a84ca81d534bb440ed44499c679b735c`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb30ab0381f972446c4a3a76800baeaed540a565f4be520f34a34f2a7a64725e`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b0743f876d33a9f1de8b5a0aaa3f2a734c9474321a52212480c2a112d2d8f`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd96b185b287f7b5d69054fb89fcb5346622ddbd660f9696713673a2b2f1c5c2`  
		Last Modified: Wed, 13 May 2026 19:05:03 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6222a2c0551ea559c3a9de786436992430f2ba3c37f02deeb29a95be167e02e`  
		Last Modified: Wed, 13 May 2026 19:05:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8a9db2a53fdd31659167bac43beed8c9eeb69b82db02d44fb2d3781caaeb7089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.3 KB (505258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bea2f2eafe0087b0cfd9762947ff4969bf53ba0eb053c36c87006206dc6377f`

```dockerfile
```

-	Layers:
	-	`sha256:08608661eebece92e72ee99c418b75a5349948d8bad8b50c06a8580bc375ece9`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 473.5 KB (473490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f45673aaecae2389d111459eb870bf2e1a8e833b5bf0547d5387b40c28469cb`  
		Last Modified: Wed, 13 May 2026 19:05:02 GMT  
		Size: 31.8 KB (31768 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:3f4ec44134ac286226432d9a75befb2fae397b48c20cd508c967b10bad62f521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5639832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da685248acfd92dd3dc91cc5d930097ae104138b9fe1e90484ec65f5a056f33e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 22:21:36 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 15 Apr 2026 22:21:36 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 22:21:36 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 22:21:36 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 22:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:21:36 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 22:21:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 22:21:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790c9626838b16c3565d1bcfc03e259d5688740183c6c87086432fb1246b4d28`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 1.9 MB (1944800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42711eaa950d5ab61e9b0decb8cdfd0d60777c4588f544817ba24947a051572`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e6db7a108207bdf04bd1497b2d14bdd5304cd5c92deaac1cd5143209678315`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b053fb46bb24a68a876bc128a5d9089dfc3a354668d4e0aca2ef27143e77aecd`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741544632639e3995f110616119c52679d83b71df3ee830d4e516e8c5e245b14`  
		Last Modified: Wed, 15 Apr 2026 22:21:42 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916e7020bd3eb4a018a802cd5ee71f707b3b4c45a33fc2bacec1979e321e141f`  
		Last Modified: Wed, 15 Apr 2026 22:21:42 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:008c7efd2200ce668d9f66e7840a606e22f64d048883acf45da2bb93a836b04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.5 KB (505488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b4ad9fe2feb9e1833759dab8d244a0a2096e8340646321373d49490b75d2de`

```dockerfile
```

-	Layers:
	-	`sha256:d5b6db83c7159e031b964ed76e668b7fa0ae198ffe49f06aa0ca67c7f0d96fd2`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 474.0 KB (473957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60cf70f9993b75b8184a8db90f6aaf37ef1f9f8d6408fc5a425bba1886acd9ba`  
		Last Modified: Wed, 15 Apr 2026 22:21:41 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:b79407001771668e1bd40af7347f4cf9deb1d779ce7ab02f1fe0f437a24830d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dadf1a56b0a7389b47a0b8890a544893147c533fe1cadc92eccc7d515b02e74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:04:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:04:25 GMT
ENV NGINX_VERSION=1.31.0
# Wed, 13 May 2026 19:04:25 GMT
ENV PKG_RELEASE=1
# Wed, 13 May 2026 19:04:25 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 May 2026 19:04:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:04:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:27 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:04:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:04:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:04:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec4312ca83c32a631a958182b9d9793a07e75ccf5398cb55538dd5f974a92c`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 2.0 MB (1975194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415fe7616dd134763e31fc34a6afeb36a2b180a615a3687e46d523951b820f05`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728b0b1798394d7d813c666fc1563a8823ba009e074d8a869e9f1a20113a9fb6`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16c30b6d8a924c1e0b4565211de505e808f6d46947ec87a4e850dfbfde39f5`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f85dab021f5ff2707e41a5c82cc8d6ec735f22de4025605be9338ea286978a5`  
		Last Modified: Wed, 13 May 2026 19:04:46 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b092a9079ff9a2081e962be84308b0ae95af06c9cba269756363ba71e6f1b05`  
		Last Modified: Wed, 13 May 2026 19:04:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9058055782b2b6be1f53fb24c18ff20e0a12f0ecde98bfd93799884bf110bc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 KB (505104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733d890730e19d390b310fc744c2fdf6fc2baa9819a4efe948c3783dafb1c640`

```dockerfile
```

-	Layers:
	-	`sha256:cd2b2e62d266ba9baa056151127c32c2f48fb8022654fca9e80e141a82966fea`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 473.4 KB (473431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452d01f1b98d9da036054c8dfaaee9d93a02e051f7060f035aae5d77db64c16f`  
		Last Modified: Wed, 13 May 2026 19:04:45 GMT  
		Size: 31.7 KB (31673 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:b7bcfeb977e408ab7f4d6a01f4c0a6034c593c2337a764d755eb948b349387ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5510150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe28ef0792dbc801c80a372025b23b6e4b34ab07b9b9bec58dbe24c6f04da812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:59:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 23:59:37 GMT
ENV NGINX_VERSION=1.29.8
# Wed, 15 Apr 2026 23:59:37 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 23:59:37 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 23:59:37 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 23:59:37 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 23:59:38 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 23:59:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:59:38 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 23:59:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 23:59:38 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5facb7227451ad08eff6bb7d434d04407e9e896052270c23a7d8aeb731012b`  
		Last Modified: Thu, 16 Apr 2026 00:00:15 GMT  
		Size: 1.9 MB (1917890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e30c482440b1ed34153e68bc661a9cb432ec9daf32980b4ea6d70bd97a0f84`  
		Last Modified: Thu, 16 Apr 2026 00:00:16 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019124b3987bd1389111dd4cb32f5226951980f847fdab9caba07a94071ca493`  
		Last Modified: Thu, 16 Apr 2026 00:00:15 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b9986e78b521af5160a5fc29bcedf6cdecaf72f3a314359f673aaf2fd821fd`  
		Last Modified: Thu, 16 Apr 2026 00:00:15 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0547fdff6c9ca81c5726869566dc868e67e7b2124b601f6094de9207db2898d`  
		Last Modified: Thu, 16 Apr 2026 00:00:17 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4685d3d794fe282e5c08eee10f8e45e003b201ae378fb6bd6b00396c28201`  
		Last Modified: Thu, 16 Apr 2026 00:00:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8705576872ac9c8157336ca7bcd06498c67b0dcafd1fcd1ed6944fb1d5966107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 KB (505100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a05ed99fea2f4ead7046be6979eb6b8aae9b85f3a6b49b764fb50891f2c049e`

```dockerfile
```

-	Layers:
	-	`sha256:956bb231b7385d318fe05a71a75250515501943405dffdd13a71fc66289b5354`  
		Last Modified: Thu, 16 Apr 2026 00:00:17 GMT  
		Size: 473.4 KB (473427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f948e73a1894aa8e708d256e9ab1ff76e4d1bd15be0e010b98ddf05e102e72e`  
		Last Modified: Thu, 16 Apr 2026 00:00:14 GMT  
		Size: 31.7 KB (31673 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:218f26419794c66873b1f7fc943a0af7c87d049951a58e733c75cb542eaf758d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b3faf3924b34cf02ca24eac03b3d01a00aaf89eb995f971be72e5e2d52d93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 19:04:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:04:25 GMT
ENV NGINX_VERSION=1.31.0
# Wed, 13 May 2026 19:04:25 GMT
ENV PKG_RELEASE=1
# Wed, 13 May 2026 19:04:25 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 May 2026 19:04:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:04:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:04:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:04:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:04:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4bb606918769b8447a1e82d0d7253d533d59e1d35d8599b037e42d1c0e9ebb`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 2.0 MB (2003805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8b4b99509ff9f8af894a06a74e48a1b03872a63acefb2d040f1fc78a03559`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d7edea433ba4697ce5ab1c0d7e7df79c8dd134f7f252814fdf241e9c1275b`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48df14e389b6d8bee974ac3e39b15ad1b73432668f6d23c4bc980468e64ec184`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b396c46b71b289806d89f1c2372fcd5787bb5684d47698ddf0070996e93508a`  
		Last Modified: Wed, 13 May 2026 19:04:36 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886eb4e010dbfbcf8588dafc05e5c0c2f385a3ac8de811d23b827dbc4d87b14`  
		Last Modified: Wed, 13 May 2026 19:04:36 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9fd12fd95602044fd082aa09395a4edc7392bcab4658de37ea7f1a9d50f8e175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.0 KB (504954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded27d84deb8e3680ba5e1fbf62c6921b79b282a3003121d4a1b13637fdec424`

```dockerfile
```

-	Layers:
	-	`sha256:ce1119224d68a36416dfec4521514246b12253a506f96c8739b7fa3bfcc0eea3`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 473.4 KB (473361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c138821f7d1896dd8fee562c0a4ed8e99e2e38f95856125b12240ee1c059fe`  
		Last Modified: Wed, 13 May 2026 19:04:35 GMT  
		Size: 31.6 KB (31593 bytes)  
		MIME: application/vnd.in-toto+json
