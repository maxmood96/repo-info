## `nginx:stable-alpine3.23-slim`

```console
$ docker pull nginx@sha256:d5b51cfc7d55fc7a7bcf4d1d577b9c3738331df56d68f0b1d8ac9795b9470a5a
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

### `nginx:stable-alpine3.23-slim` - linux; amd64

```console
$ docker pull nginx@sha256:25fb954ff92e905e92c7284c6d32d8ac733eb3e318eb1dc99faff7987f825388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5720535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64aa06ec89593328b99416e0381f0c52633518b9ec945d36c6e31dbdd696d24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:46:34 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:46:34 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:46:34 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:46:34 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:34 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:46:34 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:46:34 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb20213977c1182954baceb40b9c0817823a61b284716ae1fa87a94f99a393`  
		Last Modified: Mon, 22 Jun 2026 19:46:40 GMT  
		Size: 1.9 MB (1871516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79d40162f281479a472d6d2ec1b998ff1c2223c0e58305377d20a40b1c2298d`  
		Last Modified: Mon, 22 Jun 2026 19:46:40 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9cfad643ec786c3f1615bf34e06ab3db76bd608ad45596fa80ce280f845713`  
		Last Modified: Mon, 22 Jun 2026 19:46:40 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278fa14e43da8662fc63fb54817d89af38d827e0b48d96b42f98aa856216b81a`  
		Last Modified: Mon, 22 Jun 2026 19:46:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264ebfe1e4251ad76c8fd2afe6195e806268c4e21ba61a54695d075e3bf39fe`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440503bb46cabd1979a41645dbbc263ef369a604b30bac3652848206e7108bbd`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8dbf03b232b4ccdf283d57f0332da5ff0f04d1965a727a79e56dce317e3def6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.0 KB (503045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fa45a04dca88a2cbceab461e3a78fc8151ee617b0548dd44c55676904b7c4e`

```dockerfile
```

-	Layers:
	-	`sha256:82ff3116c01a336c521422dbaa7b86b65023944466baefed214da93bef5c945e`  
		Last Modified: Mon, 22 Jun 2026 19:46:40 GMT  
		Size: 472.8 KB (472756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ff40276faca87a70efd3b719235955d4f8ba7c46bc3fe8b0d2fe1f07703fdf`  
		Last Modified: Mon, 22 Jun 2026 19:46:39 GMT  
		Size: 30.3 KB (30289 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:3096c283af6b726fef28239780a5bc8ffa0441d8a247ee03c569d5f8b60e229f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc5f17e555e2326e32c8bf54d3839a1bd2861b7163cb633c7865f4b71d74548`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:46:49 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:46:49 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:46:49 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:46:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:46:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:50 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:46:50 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:46:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01463aecd1411b146b2b854f10429d3c47b9445bfafd8786f88bcff7befb26`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 1.9 MB (1870052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38b193ea1e3f5c29006bd3db90878c4937f01be4a719d5d39f2ca5a2b921d36`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a0c976842b79fa5d0f00409fb9fbdb6fde91393b45726d672de41c5cd39b41`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a92e66bd6263ce23725904bce896f4286595a15cbffdd6cf251a00de14f830`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b37069556d61d0a8279ed99567f6d38cc6f36677cf54c26eaea29fb6a7693d2`  
		Last Modified: Mon, 22 Jun 2026 19:46:55 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bcaaf579f6aa12f0522440cc0af7798bb734222a01313606e7efda7fc62139`  
		Last Modified: Mon, 22 Jun 2026 19:46:55 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1b4a93c8b35c86cadfafdcf8de3e8e1e03fef57770228563498bf03653cf98e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858a546b457a07e0138f924600aec2c01f21b62afc184506d0de57b44d6a1360`

```dockerfile
```

-	Layers:
	-	`sha256:18158eb505a159a525506b91b47bb6ae866c09a89144ebd846fbb411d26a763a`  
		Last Modified: Mon, 22 Jun 2026 19:46:54 GMT  
		Size: 30.2 KB (30170 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b3a22ddecd7bac3d29fa77ed498f4bab01b813086c56e85be9c656bb8fae6c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6391cffe2c1fdcf7b6046e3207d2846edc2aa2c06519bf152afa907ca44330`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:56:05 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:56:05 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:56:05 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:56:05 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:56:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:05 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:56:05 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:56:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dfe7e8e56af55eec629338cc35dd0bd46f1aa5bbb97c8b6e5f52166477aa89`  
		Last Modified: Mon, 22 Jun 2026 19:56:11 GMT  
		Size: 1.7 MB (1694634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d9b5331c9ef136e72ea57ad25d56ec98b6369f2bc994d3237ccb38951b0ebb`  
		Last Modified: Mon, 22 Jun 2026 19:56:10 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9231b9fe7ba5cac4613bb686a9d39deea38614d80f4d1381bf463726ed395a6d`  
		Last Modified: Mon, 22 Jun 2026 19:56:10 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec682ca53b4e1dacac485a5a9c6b44e2f6d21ebf09e544bb135ce86e72bddb4`  
		Last Modified: Mon, 22 Jun 2026 19:56:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46145cae015d297e5e87bf2b23d3550744baa60675ed2560dbcc6b7ea06f504b`  
		Last Modified: Mon, 22 Jun 2026 19:56:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6228625365b52971ed1450ca0acc23aefa74a20446686a49d2e381ab49b16915`  
		Last Modified: Mon, 22 Jun 2026 19:56:12 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:20c36fd7a6581ab5cd96cb06594e18bcf2a927a5d8a7c7db14122ba14a7043c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4026958f1ba4b8f1b6ff1bd49f4391d4381803564c5bb609bc69837ed7025f18`

```dockerfile
```

-	Layers:
	-	`sha256:6a442174c821001878832f8b108b4f6b787992191ff135f1736b588d64fd4b16`  
		Last Modified: Mon, 22 Jun 2026 19:56:11 GMT  
		Size: 472.2 KB (472158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057925e2452edc639f930b85ff6c677797ed1e83f4d1a1af29a34b3c616ebc7c`  
		Last Modified: Mon, 22 Jun 2026 19:56:10 GMT  
		Size: 30.4 KB (30384 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:914c8aba871dc6daabfd97df8c868e2af9ffa19eb6165120856a941d2cee72c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d86511f5da3eabdafe8786973e364ffbafb671194a0361015952a883b8d51a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:47:21 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:47:21 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:47:21 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:47:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:47:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:47:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2037b3b08c3c199319f035a8b35da6da24c6ae573a19369878bc50eacf6592`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 1.9 MB (1892639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80af2fb514ce4eda14fdbe9029105c9bd0fec13e9b68b66629d141d7d732ac7c`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254cd492ba6baa2ab643a48acc8d9900b352b646085ba38a6f6eddac2f2196ec`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6da3f4ebec2a6cf2c3e4269b88f54c7159a641d82b301a0ae16f4b659be542e`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74b1f21fac2c4b73eca07ccd555daf6287c59397bcf4a1993cfe4777947c257`  
		Last Modified: Mon, 22 Jun 2026 19:47:28 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc683ae8fd6bbe98aa0b5c103597a173845ce66a84cc2144cf2cf28c1e40f65`  
		Last Modified: Mon, 22 Jun 2026 19:47:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e8d13d2e38b75859735e121008055c417f5ab875bcd4c1f6276918b3bcd0b529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.6 KB (502603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfca40e5921b12c99cdcc0e9f335c068bf3c99f30ea6621519e37766ecd487ff`

```dockerfile
```

-	Layers:
	-	`sha256:4ee8d28348821064e2f7b9b96f06d1343f632315271f2bf9f9173b4ef1d7e175`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 472.2 KB (472186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2bdec3fc49c164e048bb26af189b26cb804e91306434b5c95a78e36b270f5d`  
		Last Modified: Mon, 22 Jun 2026 19:47:27 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:a1d7ac63cdd1175c6bb543b06036f14bc10f857beee2fb5d83c47ae0a82bbd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883b5fe7488f479b562a68f614c13463888f2c374363f7f6ef61eff17b0ae2a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:13 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:47:13 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:47:13 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:47:13 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:47:13 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dce2a039f88eb39a8d139a1cd5e4499efc2bf8ab91ab9c57929a6b74e3c6970`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 1.9 MB (1945389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e03539862017893aa038ed90f9bc27ff174b22d530b1943a5369de326301c`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddc59961ca05ffd35110d6bf0c1f4424cc132bc55933354d9cc24d07df45d2e`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e8a175e96709f72f70362015e16afb4b20c50d1346aaade74458ff1332f141`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab604220382c713aab538df57eaee7add13498c38a689f56b0e8ffdf48c57110`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7629014b6ab4c782b8eb4c563876c03fd8f9633e6e42211e802f1a64393c9eb4`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:43f76a3feb6abb36fe2cc8753fdeee3e6a78b5dd616bfc56624e7b6aeb7c0768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.0 KB (502968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3152cf3ecf88edc19ad62d8cba6e46b58f21641dd047797b4da7f032c974f5b6`

```dockerfile
```

-	Layers:
	-	`sha256:c9287b2ae7a307b69208acde90c3f8e75840a21ea59523c9bdba8cf0abdc1ad6`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 472.7 KB (472721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f5e856002162c08c1958d4c679ba5f5fb4c8abd9a5a95f57189c16cc24c48a`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 30.2 KB (30247 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:a1082630598562127c164af07be763b88d34ec8c557c317caf86cc577c183432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccffb0ab904f3d1f1048ea60f3396f35e2ac53bb5d13e7e21db5049f76597d40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:02 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:55:02 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:55:02 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:55:02 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:55:02 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:55:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:55:03 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:55:03 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:55:03 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:55:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:55:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:04 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:55:04 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:55:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9504e463654e9e8a314cb2e50b271352b27b39edd95d26f9c86ba0a1f939468`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 2.0 MB (1963699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62765bb13d037366a54a2698fb4939446d6a4c8c52758fad8b989d64abe16d49`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b9205de98209dd9add6fdcaf9ef7e8cfcad4440a4fc87099809112d456e606`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfd2e672617d124fbaa974101ac2815f80904f0c3da59e2e314ea63d86f438d`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f64f68b7baafe1423e44f5c326c79c40bb59e2caaef1798a92188ed1d3358cd`  
		Last Modified: Mon, 22 Jun 2026 19:55:22 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9320fe1155a261c2a4d08edf34eb6c149f6609815fd4fd64727d46c9737f743f`  
		Last Modified: Mon, 22 Jun 2026 19:55:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1034114f4fcb6ada27d4dbf3740037cc97158275b3931e3cfda31a45b541e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008a5307ddc5bf3f9e3c0dc2933816d034620e8dddb9e03ca3433a59c1059d5e`

```dockerfile
```

-	Layers:
	-	`sha256:2acdd4de59326e0607314e4e080c36fc3357e2c351f8fb7a320791992c5f94c4`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 472.2 KB (472151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94c30c842fd02ce540dab781f4df65ebd475eb18f2643997f15aa40fcca63e1`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 30.3 KB (30345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:4e037570db45a8f271e57bc53ed8703cc950af5c70d2b18394cdb61307cf256d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5496310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b173127346b0d379bd5da42f0958886dc50ffda34c152b49a3d467c545df5795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:36:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 21:36:25 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 21:36:25 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 21:36:25 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 21:36:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 21:36:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 21:36:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 21:36:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 21:36:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 21:36:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 21:36:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 21:36:26 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 21:36:26 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 21:36:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a717aec409445e8bb2769ceb1d821eb33efc20601f3a7f5e062bf4e35464d67`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 1.9 MB (1918465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161c78305dfb370c40fc46637563431a75645f9194748570ab1adf0c5493929e`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc54fc980caa529d464100a9a3978a978516611755ff19d2d2d14be3d9cfac`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc696d8d85a840f5dfa1746c54246511138875c83b68ee35022548646e8170`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8238b91dd1a834c571fa0c8f14877c524f9fe26d20055c6249d3fe23d76d4f`  
		Last Modified: Mon, 22 Jun 2026 21:36:52 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1bc0aa0ecc09ea06faa239d3e3489534d8323d3dbe7441b8a0d3229d3899e`  
		Last Modified: Mon, 22 Jun 2026 21:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8059d1d42df451c11764bbdd82be9fab94aa223b642b83fc700eda0cebc4647c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff82839866034c8e376eb2db55fa0236dd13a6dd3ec1aad1ad5aaa437bb56b06`

```dockerfile
```

-	Layers:
	-	`sha256:a478e459088b1f761896c614446c62b1eaf547378c68dec1200137d1196b6e2b`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 472.1 KB (472147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2416a98cbad326730093bdade1bcf4e7d41750def2ddc07fb4f6b31c04534a96`  
		Last Modified: Mon, 22 Jun 2026 21:36:51 GMT  
		Size: 30.3 KB (30345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:ab8defdbec55e1f85e83dc0034ed14138371247783a3aa7c0e2d095408b06f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741382f03cbcb52b885127b2c98ebdcefd6a0a7cfd7635a8113a558847aec79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:48:22 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 22 Jun 2026 19:48:22 GMT
ENV NGINX_VERSION=1.30.3
# Mon, 22 Jun 2026 19:48:22 GMT
ENV PKG_RELEASE=1
# Mon, 22 Jun 2026 19:48:22 GMT
ENV DYNPKG_RELEASE=1
# Mon, 22 Jun 2026 19:48:22 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 22 Jun 2026 19:48:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:48:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 22 Jun 2026 19:48:22 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Jun 2026 19:48:22 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b227c1f355078966dc636c81ef5cff783f4de634afeb94624d2b672f869850`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 2.0 MB (1991134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35f125d1a98b3ab710459f8d0032a53e62b2e157386cb6f2e26910eb7e7343a`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a92391cba4bfe646e0d47e3c77b4fb881e5024d8e0d43b3545cbd72d472aa`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4469e551c7c1bde1eaef8f7a8180c12fc2cbd324416c4c2246df4b5161092e`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91c0c94bb9ac919e3fca0a5324a4f7b071e154311544d1fd2a6803ff8e08b8`  
		Last Modified: Mon, 22 Jun 2026 19:48:32 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc48f26abb444b8cdb5147d80c6fe86362c319a3b555a9a7189f075d0f13a2b`  
		Last Modified: Mon, 22 Jun 2026 19:48:32 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3407b02b37ef23540de5e9f0d48f27bb5b64bff4be188fd18142826bc08e8303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5119f421a66902cee68ce9b4f58df16cd732008bd5f759075d98197d6251bd2`

```dockerfile
```

-	Layers:
	-	`sha256:8fdb7b1f6833d09f943ea5795903719b361b197c66d5db24dcc4b856af986242`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 472.1 KB (472105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae351a33190d6100e19c35bbc479c0f17fa620d26ade2278750922af2a22ea37`  
		Last Modified: Mon, 22 Jun 2026 19:48:31 GMT  
		Size: 30.3 KB (30289 bytes)  
		MIME: application/vnd.in-toto+json
